# Copyright Materialize, Inc. and contributors. All rights reserved.
#
# Use of this software is governed by the Business Source License
# included in the LICENSE file at the root of this repository.
#
# As of the Change Date specified in that file, in accordance with
# the Business Source License, use of this software will be governed
# by the Apache License, Version 2.0.

MZFROM ubuntu-base

RUN apt-get update && apt-get -qy install \
    ca-certificates \
    wait-for-it

COPY kdestroy kinit testdrive /usr/local/bin/

WORKDIR /workdir

RUN mkdir -p /share/tmp && chmod 777 /share/tmp
RUN mkdir -p /share/mzdata && chmod 777 /share/mzdata

VOLUME /share/tmp
VOLUME /share/mzdata

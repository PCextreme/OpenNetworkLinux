############################################################
# <bsn.cl fy=2014 v=onl>
#
#           Copyright 2014 BigSwitch Networks, Inc.
#
# Licensed under the Eclipse Public License, Version 1.0 (the
# "License"); you may not use this file except in compliance
# with the License. You may obtain a copy of the License at
#
#        http://www.eclipse.org/legal/epl-v10.html
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
# either express or implied. See the License for the specific
# language governing permissions and limitations under the
# License.
#
# </bsn.cl>
############################################################
#
#
############################################################
include $(ONL)/make/config.amd64.mk

MODULE := libonlp-x86-64-accton-as7926-80xk
include $(BUILDER)/standardinit.mk

DEPENDMODULES := AIM IOF x86_64_accton_as7926_80xk onlplib
DEPENDMODULE_HEADERS := sff

include $(BUILDER)/dependmodules.mk

SHAREDLIB := libonlp-x86-64-accton-as7926-80xk.so
$(SHAREDLIB)_TARGETS := $(ALL_TARGETS)
include $(BUILDER)/so.mk
.DEFAULT_GOAL := $(SHAREDLIB)

GLOBAL_CFLAGS += -I$(onlp_BASEDIR)/module/inc
GLOBAL_CFLAGS += -DAIM_CONFIG_INCLUDE_MODULES_INIT=1
GLOBAL_CFLAGS += -fPIC
GLOBAL_LINK_LIBS += -lpthread

include $(BUILDER)/targets.mk


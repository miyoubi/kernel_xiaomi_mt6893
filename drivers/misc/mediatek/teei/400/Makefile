# Copyright (c) 2015-2020, MICROTRUST Incorporated
# All Rights Reserved.
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License
# version 2 as published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.

subdir-ccflags-y  += -I$(src)/common/include

subdir-ccflags-y  += \
	-I$(src)/tz_dcih \
	-I$(src)/public \
	-I$(src)/tz_driver/include

ifeq ($(CONFIG_MTPROF), y)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/mtprof/
endif

subdir-ccflags-$(CONFIG_MICROTRUST_DEBUG) += -DDEBUG

obj-y += tee/
obj-$(CONFIG_MICROTRUST_TZ_DRIVER) += tz_driver/
obj-$(CONFIG_MICROTRUST_VFS_DRIVER) += tz_vfs/
obj-$(CONFIG_MICROTRUST_FP_DRIVER) += teei_fp/
obj-$(CONFIG_MICROTRUST_KEYMASTER_DRIVER) += ut_keymaster/
obj-y += tz_dcih/
obj-$(CONFIG_MICROTRUST_TEST_DRIVERS) += tests/
obj-$(CONFIG_MICROTRUST_UNITTEST_SUPPORT) += ut_tester/

# add -Wall to try to catch everything we can.
ccflags-y += -I$(src)

ifneq ($(filter m y,$(CONFIG_INPUT_EGISTEC_FPS_NAVI_HORIZON)),)
	ccflags-y += -DCONFIG_INPUT_EGISTEC_FPS_NAVI_HORIZON
endif

ets_fps_mmi-y += ets_fps.o

ifneq ($(filter m y,$(CONFIG_INPUT_EGISTEC_FPS_NAVI)),)
	ccflags-y += -DCONFIG_INPUT_EGISTEC_FPS_NAVI
	ets_fps_mmi-y += ets_navi_input.o
endif
ifneq ($(filter m y,$(CONFIG_INPUT_EGISTEC_FPS_NAVI_VERTICAL)),)
	ccflags-y += -DCONFIG_INPUT_EGISTEC_FPS_NAVI_VERTICAL
endif
ifeq ($(TARGET_BUILD_VARIANT),userdebug)
	ccflags-y += -DFP_SPI_DEBUG
endif

obj-$(FINGERPRINT_EGISTEC_FPS_MMI) += ets_fps_mmi.o

ifneq ($(filter 0 90 180 270,$(CONFIG_INPUT_EGISTEC_FPS_POSE)),)
	ccflags-y += -DCONFIG_INPUT_EGISTEC_FPS_POSE=$(CONFIG_INPUT_EGISTEC_FPS_POSE)
endif

ifneq ($(filter m y, $(CONFIG_EGIS_DISPLAY_SPEED_UP)),)
ccflags-y += -DCONFIG_EGIS_DISPLAY_SPEED_UP
endif

ifneq ($(filter m y, $(CONFIG_NAV_DOUBLE_TAP)),)
ccflags-y += -DCONFIG_NAV_DOUBLE_TAP
endif

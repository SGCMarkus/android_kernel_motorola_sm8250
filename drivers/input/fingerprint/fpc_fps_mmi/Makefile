# add -Wall to try to catch everything we can.
ccflags-y += -I$(src)

ifneq ($(filter m y,$(CONFIG_INPUT_MISC_FPC1020_SAVE_TO_CLASS_DEVICE)),)
	ccflags-y += -DCONFIG_INPUT_MISC_FPC1020_SAVE_TO_CLASS_DEVICE
endif

fpc1020_mmi-y += fpc1020_tee.o

obj-$(CONFIG_FINGERPRINT_FPC_TEE_MMI) += fpc1020_mmi.o

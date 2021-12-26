# add -Wall to try to catch everything we can.
ifneq ($(filter m y,$(CONFIG_AF_NOISE_ELIMINATION)),)
	EXTRA_CFLAGS += -DCONFIG_AF_NOISE_ELIMINATION
endif

obj-$(CONFIG_MISC_AW8695) += aw8695.o
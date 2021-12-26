ifneq ($(filter m y,$(CONFIG_PD_CHARGER_MMI)),)
	ccflags-y += -DCONFIG_PD_CHARGER_MMI
endif

ifneq ($(filter m y, $(CONFIG_BQ2597X_DUAL)),)
	ccflags-y += -DCONFIG_BQ2597X_DUAL
endif

obj-$(CONFIG_QPNP_SMBCHARGER_MMI) += qpnp-smbcharger-mmi.o
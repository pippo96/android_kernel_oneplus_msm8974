#
# Makefile for the Linux kernel device drivers.
#
# 15 Sep 2000, Christoph Hellwig <hch@infradead.org>
# Rewritten to use lists instead of if-statements.
#

# GPIO must come after pinctrl as gpios may need to mux pins etc
obj-y				+= pinctrl/
obj-y				+= gpio/
obj-$(CONFIG_PCI)		+= pci/
obj-$(CONFIG_PARISC)		+= parisc/
obj-$(CONFIG_RAPIDIO)		+= rapidio/
obj-y				+= video/
obj-y				+= idle/
obj-$(CONFIG_ACPI)		+= acpi/
obj-$(CONFIG_SFI)		+= sfi/
# PnP must come after ACPI since it will eventually need to check if acpi
# was used and do nothing if so
obj-$(CONFIG_PNP)		+= pnp/
obj-$(CONFIG_ARM_AMBA)		+= amba/
# Many drivers will want to use DMA so this has to be made available
# really early.
obj-$(CONFIG_DMA_ENGINE)	+= dma/

obj-$(CONFIG_VIRTIO)		+= virtio/
obj-$(CONFIG_XEN)		+= xen/

# regulators early, since some subsystems rely on them to initialize
obj-$(CONFIG_REGULATOR)		+= regulator/

# tty/ comes before char/ so that the VT console is the boot-time
# default.
obj-y				+= tty/
obj-y				+= char/

# gpu/ comes after char for AGP vs DRM startup
obj-y				+= gpu/

obj-$(CONFIG_CONNECTOR)		+= connector/

# i810fb and intelfb depend on char/agp/
obj-$(CONFIG_FB_I810)           += video/i810/
obj-$(CONFIG_FB_INTEL)          += video/intelfb/

obj-$(CONFIG_PARPORT)		+= parport/
obj-y				+= base/ block/ misc/ mfd/ nfc/
obj-$(CONFIG_NUBUS)		+= nubus/
obj-y				+= macintosh/
obj-$(CONFIG_IDE)		+= ide/
obj-$(CONFIG_SCSI)		+= scsi/
obj-$(CONFIG_ATA)		+= ata/
obj-$(CONFIG_TARGET_CORE)	+= target/
obj-$(CONFIG_MTD)		+= mtd/
obj-$(CONFIG_SPI)		+= spi/
obj-$(CONFIG_SPMI)		+= spmi/
obj-$(CONFIG_SLIMBUS)		+= slimbus/
obj-y				+= hsi/
obj-y				+= net/
obj-$(CONFIG_ATM)		+= atm/
obj-$(CONFIG_FUSION)		+= message/
obj-y				+= firewire/
obj-$(CONFIG_UIO)		+= uio/
obj-y				+= cdrom/
obj-y				+= auxdisplay/
obj-$(CONFIG_PCCARD)		+= pcmcia/
obj-$(CONFIG_DIO)		+= dio/
obj-$(CONFIG_SBUS)		+= sbus/
obj-$(CONFIG_ZORRO)		+= zorro/
obj-$(CONFIG_MAC)		+= macintosh/
obj-$(CONFIG_ATA_OVER_ETH)	+= block/aoe/
obj-$(CONFIG_PARIDE) 		+= block/paride/
obj-$(CONFIG_TC)		+= tc/
obj-$(CONFIG_UWB)		+= uwb/
obj-$(CONFIG_USB_OTG_UTILS)	+= usb/
obj-$(CONFIG_USB)		+= usb/
obj-$(CONFIG_PCI)		+= usb/
obj-$(CONFIG_USB_GADGET)	+= usb/
obj-$(CONFIG_SERIO)		+= input/serio/
obj-$(CONFIG_GAMEPORT)		+= input/gameport/
obj-$(CONFIG_INPUT)		+= input/
obj-$(CONFIG_I2O)		+= message/
obj-$(CONFIG_RTC_LIB)		+= rtc/
obj-y				+= i2c/ media/
obj-$(CONFIG_PPS)		+= pps/
obj-$(CONFIG_PTP_1588_CLOCK)	+= ptp/
obj-$(CONFIG_W1)		+= w1/
obj-$(CONFIG_POWER_SUPPLY)	+= power/
obj-$(CONFIG_HWMON)		+= hwmon/
obj-$(CONFIG_THERMAL)		+= thermal/
obj-$(CONFIG_WATCHDOG)		+= watchdog/
obj-$(CONFIG_MD)		+= md/
obj-$(CONFIG_BT)		+= bluetooth/
obj-$(CONFIG_ACCESSIBILITY)	+= accessibility/
obj-$(CONFIG_ISDN)		+= isdn/
obj-$(CONFIG_EDAC)		+= edac/
obj-$(CONFIG_MCA)		+= mca/
obj-$(CONFIG_EISA)		+= eisa/
obj-y				+= lguest/
obj-$(CONFIG_CPU_FREQ)		+= cpufreq/
obj-$(CONFIG_CPU_IDLE)		+= cpuidle/
obj-y				+= mmc/
obj-$(CONFIG_MEMSTICK)		+= memstick/
obj-y				+= leds/
obj-$(CONFIG_SWITCH)		+= switch/
obj-$(CONFIG_INFINIBAND)	+= infiniband/
obj-$(CONFIG_SGI_SN)		+= sn/
obj-y				+= firmware/
obj-$(CONFIG_CRYPTO)		+= crypto/
obj-$(CONFIG_SUPERH)		+= sh/
obj-$(CONFIG_ARCH_SHMOBILE)	+= sh/
ifndef CONFIG_ARCH_USES_GETTIMEOFFSET
obj-y				+= clocksource/
endif
obj-$(CONFIG_DCA)		+= dca/
obj-$(CONFIG_HID)		+= hid/
obj-$(CONFIG_PPC_PS3)		+= ps3/
obj-$(CONFIG_OF)		+= of/
obj-$(CONFIG_SSB)		+= ssb/
obj-$(CONFIG_BCMA)		+= bcma/
obj-$(CONFIG_VHOST_NET)		+= vhost/
obj-$(CONFIG_VLYNQ)		+= vlynq/
obj-$(CONFIG_STAGING)		+= staging/
obj-y				+= platform/
obj-y				+= ieee802154/
#common clk code
obj-y				+= clk/

obj-$(CONFIG_HWSPINLOCK)	+= hwspinlock/
#oppo yuyi 2013-10-11 modify begin for nfc
#ifndef CONFIG_MACH_MSM8974_14001
#obj-$(CONFIG_NFC)		+= nfc/
#else
obj-$(CONFIG_NFC_DEVICES)  += nfc/
#endif CONFIG_MACH_MSM8974_14001
#oppo yuyi 2013-10-11 modify end for nfc
obj-$(CONFIG_IOMMU_SUPPORT)	+= iommu/
obj-$(CONFIG_REMOTEPROC)	+= remoteproc/
obj-$(CONFIG_RPMSG)		+= rpmsg/

# Virtualization drivers
obj-$(CONFIG_VIRT_DRIVERS)	+= virt/
obj-$(CONFIG_HYPERV)		+= hv/

obj-$(CONFIG_PM_DEVFREQ)	+= devfreq/

#MobiCore
obj-$(CONFIG_MOBICORE_SUPPORT)  += gud/

obj-$(CONFIG_CORESIGHT)		+= coresight/

obj-$(CONFIG_BIF)		+= bif/
obj-$(CONFIG_SENSORS)		+= sensors/

# CPU quiet hotplug driver
obj-$(CONFIG_CPUQUIET_FRAMEWORK)		+= cpuquiet/

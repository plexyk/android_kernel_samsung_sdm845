#
# Makefile for caching inode integrity data (iint)
#

obj-$(CONFIG_INTEGRITY) += integrity.o

integrity-y := iint.o
integrity-$(CONFIG_INTEGRITY_AUDIT) += integrity_audit.o
integrity-$(CONFIG_INTEGRITY_SIGNATURE) += digsig.o
integrity-$(CONFIG_INTEGRITY_ASYMMETRIC_KEYS) += digsig_asymmetric.o

asflags-y += -Isecurity/integrity

subdir-$(CONFIG_IMA)			+= ima
obj-$(CONFIG_IMA)			+= ima/
subdir-$(CONFIG_EVM)			+= evm
obj-$(CONFIG_EVM)			+= evm/

subdir-ccflags-y += -Wformat

PROJECT_NAME     := blinky_nrf52840_mdk
DEFAULT_TARGET   := nrf52840_xxaa
TARGETS          := $(DEFAULT_TARGET)
OUTPUT_DIRECTORY := _build

USED_SOFTDEVICE = 0
HW_VERSION := 52

SDK_ROOT := ../../../../nrf_sdks/nRF5_SDK_15.3.0_59ac345
PROJ_DIR := ..

$(OUTPUT_DIRECTORY)/nrf52840_xxaa.out: \
  LINKER_SCRIPT  := blinky_gcc_nrf52.ld

# Source files common to all targets
SRC_FILES += \
  $(SDK_ROOT)/modules/nrfx/mdk/gcc_startup_nrf52840.S \
  $(PROJ_DIR)/main.c \
  $(SDK_ROOT)/components/boards/boards.c \
  $(SDK_ROOT)/components/libraries/util/app_error.c \
  $(SDK_ROOT)/components/libraries/util/app_error_handler_gcc.c \
  $(SDK_ROOT)/components/libraries/util/app_error_weak.c \
  $(SDK_ROOT)/components/libraries/util/app_util_platform.c \
  $(SDK_ROOT)/components/libraries/util/nrf_assert.c \
  $(SDK_ROOT)/components/libraries/strerror/nrf_strerror.c \
  $(SDK_ROOT)/modules/nrfx/mdk/system_nrf52840.c \

# Include folders common to all targets
INC_FOLDERS += \
  $(SDK_ROOT)/components \
  $(SDK_ROOT)/components/libraries/memobj \
  $(SDK_ROOT)/components/libraries/experimental_section_vars \
  $(SDK_ROOT)/components/libraries/balloc \
  $(SDK_ROOT)/components/libraries/delay \
  $(SDK_ROOT)/components/libraries/bsp \
  $(SDK_ROOT)/components/libraries/util \
  $(SDK_ROOT)/components/libraries/log \
  $(SDK_ROOT)/components/libraries/log/src \
  $(SDK_ROOT)/components/libraries/strerror \
  $(SDK_ROOT)/components/drivers_nrf/nrf_soc_nosd \
  $(SDK_ROOT)/components/boards \
  $(SDK_ROOT)/components/toolchain/cmsis/include \
  $(PROJ_DIR)/config \
  $(SDK_ROOT)/integration/nrfx \
  $(SDK_ROOT)/modules/nrfx/mdk \
  $(SDK_ROOT)/modules/nrfx/hal \
  $(SDK_ROOT)/modules/nrfx \
  $(PROJ_DIR) \

include $(PROJ_DIR)/../Makefile.common

################################################################################
# 自动生成的文件。不要编辑！
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include X-CUBE-AI/App/subdir.mk
-include Drivers/STM32U5xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := U575_CubeAI_dig_cont_0600_s3_2
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
U575_CubeAI_dig_cont_0600_s3_2.elf \

MAP_FILES += \
U575_CubeAI_dig_cont_0600_s3_2.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
U575_CubeAI_dig_cont_0600_s3_2.list \


# 所有目标
all: main-build

# 主构建目标
main-build: U575_CubeAI_dig_cont_0600_s3_2.elf secondary-outputs

# 工具调用
U575_CubeAI_dig_cont_0600_s3_2.elf U575_CubeAI_dig_cont_0600_s3_2.map: $(OBJS) $(USER_OBJS) E:\IDE\U575_CubeAI_dig_cont_0600_s3_2\STM32U575ZITXQ_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "U575_CubeAI_dig_cont_0600_s3_2.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m33 -T"E:\IDE\U575_CubeAI_dig_cont_0600_s3_2\STM32U575ZITXQ_FLASH.ld" --specs=nosys.specs -Wl,-Map="U575_CubeAI_dig_cont_0600_s3_2.map" -Wl,--gc-sections -static -L../Middlewares/ST/AI/Lib --specs=nano.specs -mfpu=fpv5-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo '已结束构建目标： $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo '已结束构建： $@'
	@echo ' '

U575_CubeAI_dig_cont_0600_s3_2.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "U575_CubeAI_dig_cont_0600_s3_2.list"
	@echo '已结束构建： $@'
	@echo ' '

# 其他目标
clean:
	-$(RM) U575_CubeAI_dig_cont_0600_s3_2.elf U575_CubeAI_dig_cont_0600_s3_2.list U575_CubeAI_dig_cont_0600_s3_2.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets

################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/MotorControl/subdir.mk
-include Drivers/STM32F3xx_HAL_Driver/subdir.mk
-include Drivers/CMSIS/subdir.mk
-include Application/User/subdir.mk
-include Application/Startup/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
003GUPIK_ROV_MOTOR.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
003GUPIK_ROV_MOTOR.list \

OBJCOPY_BIN += \
003GUPIK_ROV_MOTOR.bin \


# All Target
all: 003GUPIK_ROV_MOTOR.elf secondary-outputs

# Tool invocations
003GUPIK_ROV_MOTOR.elf: $(OBJS) $(USER_OBJS) E:\GUPIK_ROV_MOTOR_CONTROL\003GUPIK_ROV_MOTOR\STM32CubeIDE\STM32F303CBTX_FLASH.ld
	arm-none-eabi-gcc -o "003GUPIK_ROV_MOTOR.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"E:\GUPIK_ROV_MOTOR_CONTROL\003GUPIK_ROV_MOTOR\STM32CubeIDE\STM32F303CBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="003GUPIK_ROV_MOTOR.map" -Wl,--gc-sections -static -L../../MCSDK_v5.4.3/MotorControl/lib --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

003GUPIK_ROV_MOTOR.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "003GUPIK_ROV_MOTOR.list"
	@echo 'Finished building: $@'
	@echo ' '

003GUPIK_ROV_MOTOR.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "003GUPIK_ROV_MOTOR.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets

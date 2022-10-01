################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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
stm32F0_UART_Example.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
stm32F0_UART_Example.list \

OBJCOPY_BIN += \
stm32F0_UART_Example.bin \


# All Target
all: stm32F0_UART_Example.elf secondary-outputs

# Tool invocations
stm32F0_UART_Example.elf: $(OBJS) $(USER_OBJS) C:\Users\admin\STM32CubeIDE\workspace_1.3.0\stm32F0_UART_Example\STM32F051R8TX_FLASH.ld
	arm-none-eabi-gcc -o "stm32F0_UART_Example.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"C:\Users\admin\STM32CubeIDE\workspace_1.3.0\stm32F0_UART_Example\STM32F051R8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="stm32F0_UART_Example.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

stm32F0_UART_Example.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "stm32F0_UART_Example.list"
	@echo 'Finished building: $@'
	@echo ' '

stm32F0_UART_Example.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "stm32F0_UART_Example.bin"
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

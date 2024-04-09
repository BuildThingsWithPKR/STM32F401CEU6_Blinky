# STM32F401CEU6_Blinky
Blink LED with STM32 BlackPill STM32F401CEU6

Flash 256kB = 0x40000 (Final address for the Flash memory)

Conversion link:
https://www.rapidtables.com/convert/number/decimal-to-hex.html
![image](https://github.com/BuildThingsWithPKR/STM32F401CEU6_Blinky/assets/157862225/f7d26a41-262b-416c-a9c2-50448f700e0c)

Steps:
Open Cube Ide-> File -> New -> STM32 Project -> MCU/MPU Selector -> Commercial Part Number-> Enter 

![image](https://github.com/BuildThingsWithPKR/STM32F401CEU6_Blinky/assets/157862225/1f557048-9ba4-4715-8222-d1c678bf0caf)

Next ->

![image](https://github.com/BuildThingsWithPKR/STM32F401CEU6_Blinky/assets/157862225/deed3625-b87a-4782-a24c-f6909897d689)

GUI Appears!
Click on PC-13-> GPIO output
Right click PC13->Enter User Label-> STATUS_LED

![image](https://github.com/BuildThingsWithPKR/STM32F401CEU6_Blinky/assets/157862225/a85f893a-c12a-44fa-88d3-e4ed7a10458a)

System core->RCC -> HSE-> External Crystal Oscillator

![image](https://github.com/BuildThingsWithPKR/STM32F401CEU6_Blinky/assets/157862225/1e6530cf-e55b-4389-8130-8d603ec90e85)

Clock Configuration:
![image](https://github.com/BuildThingsWithPKR/STM32F401CEU6_Blinky/assets/157862225/d9ad3717-2966-4695-8887-dc0a8b3db877)

Now use Save icon to generate code.

Change the project properties to generate .bin and .hex code for flashing to MCU using Cubeprogrammer
![image](https://github.com/BuildThingsWithPKR/STM32F401CEU6_Blinky/assets/157862225/661287a4-6f02-435e-8143-ca6862e53a49)



###################################################################################
/* USER CODE BEGIN 2 */
  HAL_GPIO_WritePin(STATUS_GPIO_Port, STATUS_Pin, GPIO_PIN_SET);
  	HAL_Delay(2);

  /* USER CODE END 2 */

  /* Infinite loop */
  /* USER CODE BEGIN WHILE */
  while (1)
  {
	  HAL_GPIO_TogglePin(STATUS_GPIO_Port, STATUS_Pin);
    /* USER CODE END WHILE */

    /* USER CODE BEGIN 3 */
	  HAL_Delay(1000);
  }
  /* USER CODE END 3 */
###################################################################################

/**
  @page ADC_ADC1_DMA ADC DMA example
  
  @verbatim
  ******************** (C) COPYRIGHT 2012 STMicroelectronics *******************
  * @file    ADC/ADC1_DMA/readme.txt 
  * @author  MCD Application Team
  * @version V1.1.1
  * @date    13-April-2012
  * @brief   Description of the ADC DMA example.
  ******************************************************************************
  *
  * Licensed under MCD-ST Liberty SW License Agreement V2, (the "License");
  * You may not use this file except in compliance with the License.
  * You may obtain a copy of the License at:
  *
  *        http://www.st.com/software_license_agreement_liberty_v2
  *
  * Unless required by applicable law or agreed to in writing, software 
  * distributed under the License is distributed on an "AS IS" BASIS, 
  * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  * See the License for the specific language governing permissions and
  * limitations under the License.
  *
  ******************************************************************************
   @endverbatim

@par Example Description 

This example describes how to use the ADC1 and DMA to transfer continuously 
converted data from ADC1 to memory.
The ADC1 is configured to convert continuously ADC channel18 when using the
STM32L152-EVAL or ADC channel31 when using the STM32L152D-EVAL.

Each time an end of conversion occurs the DMA transfers, in circular mode, the
converted data from ADC1 DR register to the ADC_ConvertedValue variable.
The ADC1 clock is set to HSI (16 MHz).

@par Directory contents 

  - ADC/ADC1_DMA/stm32l1xx_conf.h    Library Configuration file
  - ADC/ADC1_DMA/stm32l1xx_it.c      Interrupt handlers
  - ADC/ADC1_DMA/stm32l1xx_it.h      Interrupt handlers header file
  - ADC/ADC1_DMA/main.c              Main program
  - ADC/ADC1_DMA/system_stm32l1xx.c  STM32L1xx system source file
  
@note The "system_stm32l1xx.c" is generated by an automatic clock configuration 
      system and can be easily customized to your own configuration. 
      To select different clock setup, use the "STM32L1xx_Clock_Configuration_V1.1.0.xls" 
      provided with the AN3309 package available on <a href="http://www.st.com/internet/mcu/family/141.jsp">  ST Microcontrollers </a>
         
@par Hardware and Software environment
  
  - This example runs on STM32L1xx Ultra Low Power High-, Medium-Density and Medium-Density Plus Devices.

  - This example has been tested with STMicroelectronics STM32L152D-EVAL (STM32L1xx 
    Ultra Low Power High-Density) and STM32L152-EVAL (STM32L1xx Ultra Low 
    Power Medium-Density) evaluation board and can be easily tailored to any 
    other supported device and development board.

  - STM32L152D-EVAL Set-up
    - Connect a variable power supply 0-3.3V to ADC Channel31 mapped on pin PF.10
      (potentiometer RV3).
    - Make sure that the Jumper JP13 is in ADC position.
    
  - STM32L152-EVAL Set-up
    - Connect a variable power supply 0-3.3V to ADC Channel18 mapped on pin PB.12
      (potentiometer RV3).
    - Make sure that the Jumper JP17 is in PB12 position.

@par How to use it ? 

In order to make the program work, you must do the following :
 - Copy all source files from this example folder to the template folder under
   Project\STM32L1xx_StdPeriph_Templates
 - Open your preferred toolchain 
 - Rebuild all files and load your image into target memory
 - Run the example

@note
- Ultra Low Power Medium-density devices are STM32L151xx and STM32L152xx 
  microcontrollers where the Flash memory density ranges between 64 and 128 Kbytes.
- Ultra Low Power Medium-density Plus devices are STM32L151xx, STM32L152xx and 
  STM32L162xx microcontrollers where the Flash memory density is 256 Kbytes.
- Ultra Low Power High-density devices are STM32L151xx, STM32L152xx and STM32L162xx 
  microcontrollers where the Flash memory density is 384 Kbytes.
    
 * <h3><center>&copy; COPYRIGHT STMicroelectronics</center></h3>
 */



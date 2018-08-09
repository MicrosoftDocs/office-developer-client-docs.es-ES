---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816893"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Hace referencia a**: Outlook 
  
Agrega una rutina de inactividad basado en función [FNIDLE](fnidle.md) al sistema de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>Parámetros

_pfnIdle_
  
> [entrada] Un puntero a la rutina de inactividad. 
    
_pvIdleParam_
  
> [entrada] Un puntero a un bloque de memoria que el motor de inactividad debe pasar como un parámetro a la rutina inactivo cuando lo llama. 
    
_priIdle_
  
> [entrada] La prioridad inicial para la rutina de inactividad. Las posibles prioridades para rutinas definido por la implementación son mayor o menor que cero, pero no es cero. La prioridad cero está reservada para un evento de usuario como un clic del mouse o un mensaje WM_PAINT. Las prioridades mayores que cero representan tareas en segundo plano que tienen una mayor prioridad a los eventos de usuario y se envían como parte del bucle de suministro de mensajes de Windows estándar. Las prioridades menor que cero representa tareas inactivas que ejecutan sólo durante el tiempo de inactividad de suministro de mensaje. Ejemplos de las prioridades son los siguientes: 1 para el envío de primer plano, 2 para la inserción de caracteres de edición de energía y 3 para la descarga de los mensajes nuevos.
    
_csecIdle_
  
> [entrada] El valor de hora inicial, en centésimas de segundo, que se usará en la especificación de parámetros de rutina inactivo. El significado del valor inicial de tiempo varía en función de lo que se pasa en el parámetro _iroIdle_ . El significado puede ser una de las siguientes opciones: 
    
  - El período mínimo de omisión de usuario que debe transcurrir antes de la MAPI motor inactivo llama a la rutina de inactividad por primera vez, si se establece la marca FIROWAIT en _iroIdle_. Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
  - El intervalo mínimo entre las llamadas a la rutina de inactividad, si se establece la marca FIROINTERVAL en _iroIdle_. 
    
_iroIdle_
  
> [entrada] La máscara de bits de indicadores que se utilizan para establecer las opciones iniciales para la rutina de inactividad. Se pueden establecer los siguientes indicadores:
    
  FIRONOADJUSTMENT
    
  > Utilice este indicador para especificar que no se debe ajustar el temporizador de rutina inactivo para la suspensión o reanudar. El comportamiento predeterminado sin esta marca es que el tiempo de espera se excluye al calcular el tiempo transcurrido. Si se pasa FIRONOADJUSTMENT el tiempo de inactividad se incluye al calcular el tiempo transcurrido.
      
  FIRODISABLED
    
  > La rutina de inactividad debe deshabilitarse cuando registrado. La acción predeterminada es permitir la rutina inactivo cuando **FtgRegisterIdleRoutine** se registra. 
      
  FIROINTERVAL 
    
  > El tiempo especificado por el parámetro _csecIdle_ es el intervalo mínimo entre las llamadas sucesivas a la rutina de inactividad. 
      
  FIROONCEONLY 
    
  > Obsoleto. No usar.  
      
  FIROPERBLOCK 
    
  > Obsoleto. No usar.  
      
  FIROWAIT 
    
  > El tiempo especificado por el parámetro _csecIdle_ es el período mínimo de omisión de usuario que debe transcurrir antes de que el motor de inactividad de MAPI llama a la rutina de inactividad por primera vez. Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
## <a name="return-value"></a>Valor devuelto

La función **FtgRegisterIdleRoutine** devuelve una etiqueta de función que identifica la rutina de inactividad que se ha agregado al sistema MAPI. Si **FtgRegisterIdleRoutine** no se puede registrar la rutina de inactividad de la aplicación de cliente o el proveedor de servicios, por ejemplo debido a problemas de memoria, devuelve NULL. 
  
## <a name="remarks"></a>Comentarios

Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) . 
  
|**Función rutina inactivo**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Se cierra el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**. 
  
Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar. No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada. 
  
El siguiente es un ejemplo del uso de la marca FIRONOADJUSTMENT en el parámetro _iroIdle_ . 
  
1. Registrar una rutina de inactividad con un retraso de 5 minutos.
    
2. Hibernación/suspensión el equipo después de 1 minuto (4 minutos en el temporizador de la izquierda).
    
3. Reanudar el equipo 10 minutos más adelante.
    
El comportamiento predeterminado, sin FIRONOADJUSTMENT, es que aún tendrá que esperar más de 4 minutos para ejecutar la rutina. Es decir, el temporizador se ha ajustado para permitir el ¿durante cuánto tiempo el equipo estaba en suspensión. Sin embargo, si se pasa FIRONOADJUSTMENT la rutina de inactividad se ejecutará en inmediatamente debido a que han transcurrido más de 5 minutos de tiempo real.
  


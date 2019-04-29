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
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418524"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega una rutina inactiva basada en la función [FNIDLE](fnidle.md) al sistema MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>Parameters

_pfnIdle_
  
> a Un puntero a la rutina inactiva. 
    
_pvIdleParam_
  
> a Un puntero a un bloque de memoria que el motor inactivo debe pasar como parámetro a la rutina inactiva cuando lo llama. 
    
_priIdle_
  
> a Prioridad inicial de la rutina inactiva. Las posibles prioridades de las rutinas definidas por la implementación son mayor o menor que cero, pero no cero. La prioridad cero se reserva para un evento de usuario, como un clic del mouse o un mensaje WM_PAINT. Las prioridades mayores que cero representan las tareas en segundo plano que tienen una prioridad mayor que los eventos de usuario y se envían como parte del bucle de bombeo estándar de mensajes de Windows. Las prioridades inferiores a cero representan las tareas inactivas que solo se ejecutan durante el tiempo de inactividad del bombeo de mensajes. A continuación se muestran ejemplos de prioridades: 1 para envío en primer plano, 2 para la inserción de caracteres de edición de energía y 3 para la descarga de mensajes nuevos.
    
_csecIdle_
  
> a El valor de hora inicial, en centésimas de segundo, que se va a usar en la especificación de los parámetros de rutina inactiva. El significado del valor de hora inicial varía en función de lo que se pasa en el parámetro _iroIdle_ . El significado puede ser uno de los siguientes: 
    
  - Período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad de MAPI llame a la rutina inactiva por primera vez, si la marca FIROWAIT está establecida en _iroIdle_. Una vez transCurrido este tiempo, el motor inactivo puede llamar a la rutina inactiva tantas veces como sea necesario. 
    
  - El intervalo mínimo entre llamadas a la rutina inactiva, si la marca FIROINTERVAL se establece en _iroIdle_. 
    
_iroIdle_
  
> a La máscara de máscara de los marcadores usados para establecer las opciones iniciales de la rutina inactiva. Se pueden establecer los siguientes indicadores:
    
  FIRONOADJUSTMENT
    
  > Use esta marca para especificar que el temporizador de rutina inactiva no debe ajustarse para suspender o reanudar. El comportamiento predeterminado sin este indicador es que el tiempo de inactividad se excluye al calcular el tiempo transcurrido. Si se pasa FIRONOADJUSTMENT, se incluye el tiempo de suspensión al calcular el tiempo transcurrido.
      
  FIRODISABLED
    
  > La rutina inactiva debe deshabilitarse cuando se registra. La acción predeterminada es habilitar la rutina inactiva cuando **FtgRegisterIdleRoutine** la registra. 
      
  FIROINTERVAL 
    
  > La hora especificada por el parámetro _csecIdle_ es el intervalo mínimo entre llamadas sucesivas a la rutina inactiva. 
      
  FIROONCEONLY 
    
  > Obsoleto. No usar. 
      
  FIROPERBLOCK 
    
  > Obsoleto. No usar. 
      
  FIROWAIT 
    
  > La hora especificada por el parámetro _csecIdle_ es el período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad de MAPI llame a la rutina inactiva por primera vez. Una vez transCurrido este tiempo, el motor inactivo puede llamar a la rutina inactiva tantas veces como sea necesario. 
    
## <a name="return-value"></a>Valor devuelto

La función **FtgRegisterIdleRoutine** devuelve una etiqueta de función que identifica la rutina inactiva que se ha agregado al sistema MAPI. Si **FtgRegisterIdleRoutine** no puede registrar la rutina inactiva de la aplicación cliente o del proveedor de servicios, por ejemplo, debido a problemas de memoria, devuelve NULL. 
  
## <a name="remarks"></a>Comentarios

Las siguientes funciones tratan con el motor inactivo de MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE](fnidle.md) . 
  
|**Función de rutina inActiva**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina inactiva registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina inactiva registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de la función devuelta por **FtgRegisterIdleRoutine**. 
  
Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse. No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad. 
  
El siguiente es un ejemplo del uso de la marca FIRONOADJUSTMENT en el parámetro _iroIdle_ . 
  
1. Registra una rutina inactiva con un retraso de 5 minutos.
    
2. Hibernar/suspender el equipo después de 1 minuto (se dejan 4 minutos en el temporizador).
    
3. Reanudar el equipo 10 minutos más tarde.
    
El comportamiento predeterminado, sin FIRONOADJUSTMENT, es que todavía tiene que esperar 4 minutos más para que se ejecute la rutina. Es decir, el temporizador se ajustó para permitir el tiempo que el equipo estuvo en modo de suspensión. Sin embargo, si pasa FIRONOADJUSTMENT, la rutina inactiva se ejecutará inmediatamente porque han transcurrido más de 5 minutos de tiempo real.
  


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
  
Agrega una rutina de inactividad basada en función [FNIDLE](fnidle.md) al sistema MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Puntero a la rutina de inactividad. 
    
_pvIdleParam_
  
> [in] Puntero a un bloque de memoria que el motor inactivo debe pasar como parámetro a la rutina de inactividad cuando lo llama. 
    
_priIdle_
  
> [in] La prioridad inicial de la rutina de inactividad. Las posibles prioridades de las rutinas definidas por la implementación son mayores o inferiores a cero, pero no cero. La prioridad cero está reservada para un evento de usuario, como un clic del mouse o un WM_PAINT mensaje. Las prioridades mayores que cero representan tareas en segundo plano que tienen una prioridad mayor que los eventos de usuario y se distribuyen como parte del bucle de bomba de mensajes Windows estándar. Las prioridades inferiores a cero representan tareas inactivas que solo se ejecutan durante el tiempo de inactividad de la bomba de mensajes. Los ejemplos de prioridades son los siguientes: 1 para el envío en primer plano, 2 para la inserción de caracteres de power-edit y 3 para descargar nuevos mensajes.
    
_csecIdle_
  
> [in] Valor de hora inicial, en centésimas de segundo, que se usará para especificar parámetros de rutina de inactividad. El significado del valor de hora inicial varía según lo que se pase en el _parámetro iroIdle._ El significado puede ser uno de los siguientes: 
    
  - Período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad MAPI llame a la rutina de inactividad por primera vez, si la marca FIROWAIT se establece en  _iroIdle_. Después de que pase este tiempo, el motor inactivo puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
  - Intervalo mínimo entre llamadas a la rutina de inactividad, si la marca FIROINTERVAL se establece en  _iroIdle_. 
    
_iroIdle_
  
> [in] Máscara de bits de las marcas usadas para establecer las opciones iniciales de la rutina de inactividad. Se pueden establecer las siguientes marcas:
    
  FIRONOADJUSTMENT
    
  > Use esta marca para especificar que el temporizador de rutina de inactividad no debe ajustarse para suspensión o reanudación. El comportamiento predeterminado sin esta marca es que el tiempo de suspensión se excluye al calcular el tiempo transcurrido. Si se pasa FIRONOADJUSTMENT, el tiempo de suspensión se incluye al calcular el tiempo transcurrido.
      
  FIRODISABLED
    
  > La rutina de inactividad debe deshabilitarse cuando se registre. La acción predeterminada es habilitar la rutina de inactividad **cuando FtgRegisterIdleRoutine** la registra. 
      
  FIROINTERVAL 
    
  > El tiempo especificado por el  _parámetro csecIdle_ es el intervalo mínimo entre las llamadas sucesivas a la rutina de inactividad. 
      
  FIROONCEONLY 
    
  > Obsoleto. No usar.  
      
  FIROPERBLOCK 
    
  > Obsoleto. No usar.  
      
  FIROWAIT 
    
  > El tiempo especificado por el parámetro  _csecIdle_ es el período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad MAPI llame por primera vez a la rutina de inactividad. Después de que pase este tiempo, el motor inactivo puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
## <a name="return-value"></a>Valor devuelto

La **función FtgRegisterIdleRoutine** devuelve una etiqueta de función que identifica la rutina de inactividad que se agregó al sistema MAPI. Si **FtgRegisterIdleRoutine** no puede registrar la rutina de inactividad para la aplicación cliente o el proveedor de servicios, por ejemplo debido a problemas de memoria, devuelve NULL. 
  
## <a name="remarks"></a>Comentarios

Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas de inactividad basadas en el prototipo de [función FNIDLE.](fnidle.md) 
  
|**Función de rutina de inactividad**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Agrega una rutina de inactividad al sistema MAPI, con o sin habilitarlo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Apaga el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de función devuelta por **FtgRegisterIdleRoutine**. 
  
Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse. No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad. 
  
A continuación se muestra un ejemplo de uso de la marca FIRONOADJUSTMENT en el _parámetro iroIdle._ 
  
1. Registrar una rutina de inactividad con un retraso de 5 minutos.
    
2. Hibernar/suspender el equipo después de 1 minuto (quedan 4 minutos en el temporizador).
    
3. Reanude el equipo 10 minutos más tarde.
    
El comportamiento predeterminado, sin FIRONOADJUSTMENT, es que aún tiene que esperar 4 minutos más para que se ejecute la rutina. Es decir, el temporizador se ajustó para permitir el tiempo que el equipo estaba dormido. Sin embargo, si pasa FIRONOADJUSTMENT, la rutina de inactividad se ejecutará inmediatamente porque han transcurrido más de 5 minutos de tiempo real.
  


---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334436"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cambia algunas o todas las características de una rutina inactiva basada en [FNIDLE](fnidle.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a>Parameters

_FTG_
  
> a Etiqueta de función que identifica la rutina inactiva. 
    
_pfnIdle_
  
> a Puntero a la rutina inactiva. 
    
_pvIdleParam_
  
> a Puntero a un nuevo bloque de memoria que asigna la implementación de la llamada a la rutina inactiva. 
    
_priIdle_
  
> a Valor que representa una nueva prioridad para la rutina inactiva. Las posibles prioridades de las rutinas definidas por la implementación son mayor o menor que cero, pero no cero. Un valor de cero se reserva para un evento de usuario, como un clic del mouse o un mensaje WM_PAINT. Los valores mayores que cero representan las prioridades de las tareas en segundo plano que tienen una prioridad mayor que los eventos de usuario y se envían como parte del bucle estándar de bombeo de mensajes de Windows. Los valores inferiores a cero representan las prioridades de las tareas inactivas que solo se ejecutan durante el tiempo de inactividad del bombeo de mensajes. Ejemplos de prioridades son: 1 para envío en primer plano, 1 para la inserción de caracteres de edición de energía y 3 para la descarga de mensajes nuevos.
    
_csecIdle_
  
> a Nueva hora, en centésimas de segundo, que se aplicará a la rutina inactiva. El significado del valor de hora inicial varía en función de lo que se pasa en el parámetro _iroIdle_ . Puede ser: 
    
  - Período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad de MAPI llame a la rutina inactiva por primera vez, si la marca FIROWAIT está establecida en _iroIdle_. Una vez transCurrido este tiempo, el motor inactivo puede llamar a la rutina inactiva tantas veces como sea necesario. 
    
  - El intervalo mínimo entre llamadas a la rutina inactiva, si la marca FIROINTERVAL se establece en _iroIdle_. 
    
_iroIdle_
  
> a Máscara de máscara de marcas que indican nuevas opciones para llamar a la rutina inactiva. Se debe establecer exactamente uno de los siguientes indicadores:
    
  - FIROINTERVAL: la hora especificada por el parámetro _csecIdle_ es el intervalo mínimo entre llamadas sucesivas a la rutina inactiva. 
      
  - FIROONCEONLY: obsoleto. No usar. 
      
  - FIROPERBLOCK: obsoleto. No usar. 
      
  - FIROWAIT: la hora especificada por el parámetro _csecIdle_ es el período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad de MAPI llame a la rutina inactiva por primera vez. Una vez transCurrido este tiempo, el motor inactivo puede llamar a la rutina inactiva tantas veces como sea necesario. 
    
_ircIdle_
  
> a Máscara de la máscara usada para indicar los cambios que se van a realizar en la rutina inactiva. Los siguientes indicadores se pueden establecer en cualquier combinación:
    
  - FIRCCSEC: un cambio en el tiempo asociado con la rutina inactiva, es decir, un cambio indicado por el valor pasado en el parámetro _csecIdle_ . 
      
  - FIRCIRO: un cambio en las opciones de la rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _iroIdle_ . 
      
  - FIRCPFN: un cambio en el puntero de rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _pfnIdle_ . 
      
  - FIRCPRI: un cambio en la prioridad de la rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _priIdle_ . 
      
  - FIRCPV: un cambio en el bloque de memoria de la rutina inactiva, es decir, un cambio que se indica mediante el valor pasado en el parámetro _pvIdleParam_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE](fnidle.md) : 
  
|**Función de rutina inActiva**|**Usage**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Cambia las características de una rutina inactiva registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina inactiva registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de la función devuelta por **FtgRegisterIdleRoutine**. 
  
Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse. No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad. 
  


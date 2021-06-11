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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418270"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cambia algunas o todas las características de una rutina de inactividad basada en [FNIDLE.](fnidle.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
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

_ftg_
  
> [in] Etiqueta de función que identifica la rutina de inactividad. 
    
_pfnIdle_
  
> [in] Puntero a la rutina de inactividad. 
    
_pvIdleParam_
  
> [in] Puntero a un nuevo bloque de memoria que la implementación de llamada asigna para la rutina de inactividad. 
    
_priIdle_
  
> [in] Valor que representa una nueva prioridad para la rutina de inactividad. Las posibles prioridades de las rutinas definidas por la implementación son mayores o inferiores a cero, pero no cero. Un valor de cero está reservado para un evento de usuario, como un clic del mouse o un WM_PAINT mensaje. Los valores mayores que cero representan las prioridades de las tareas en segundo plano que tienen una prioridad mayor que los eventos de usuario y se distribuyen como parte del bucle de bomba de mensajes Windows estándar. Los valores inferiores a cero representan las prioridades de las tareas inactivas que solo se ejecutan durante el tiempo de inactividad de la bomba de mensajes. Algunos ejemplos de prioridades son: 1 para el envío en primer plano, 1 para la inserción de caracteres de power-edit y 3 para descargar nuevos mensajes.
    
_csecIdle_
  
> [in] Una nueva hora, en centésimas de segundo, para aplicar a la rutina de inactividad. El significado del valor de hora inicial varía según lo que se pase en el _parámetro iroIdle._ Puede ser: 
    
  - Período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad MAPI llame a la rutina de inactividad por primera vez, si la marca FIROWAIT se establece en  _iroIdle_. Después de que pase este tiempo, el motor inactivo puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
  - Intervalo mínimo entre llamadas a la rutina de inactividad, si la marca FIROINTERVAL se establece en  _iroIdle_. 
    
_iroIdle_
  
> [in] Máscara de bits de marcas que indican nuevas opciones para llamar a la rutina de inactividad. Se debe establecer exactamente una de las siguientes marcas:
    
  - FIROINTERVAL: el tiempo especificado por el parámetro  _csecIdle_ es el intervalo mínimo entre las llamadas sucesivas a la rutina de inactividad. 
      
  - FIROONCEONLY: Obsoleto. No usar. 
      
  - FIROPERBLOCK: Obsoleto. No usar. 
      
  - FIROWAIT: la hora especificada por el parámetro  _csecIdle_ es el período mínimo de inacción del usuario que debe transcurrir antes de que el motor de inactividad MAPI llame a la rutina de inactividad por primera vez. Después de que pase este tiempo, el motor inactivo puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
_ircIdle_
  
> [in] Máscara de bits de las marcas que se usan para indicar los cambios que se deben realizar en la rutina de inactividad. Las siguientes marcas se pueden establecer en cualquier combinación:
    
  - FIRCCSEC: un cambio en el tiempo asociado a la rutina de inactividad, es decir, un cambio indicado por el valor pasado en el parámetro _csecIdle._ 
      
  - FIRCIRO: un cambio en las opciones de la rutina de inactividad, es decir, un cambio indicado por el valor pasado en el parámetro _iroIdle._ 
      
  - FIRCPFN: un cambio en el puntero de rutina inactiva, es decir, un cambio indicado por el valor pasado en el _parámetro pfnIdle._ 
      
  - FIRCPRI: un cambio en la prioridad de la rutina de inactividad, es decir, un cambio indicado por el valor pasado en el _parámetro priIdle._ 
      
  - FIRCPV: un cambio en el bloque de memoria de la rutina de inactividad, es decir, un cambio indicado por el valor pasado en el _parámetro pvIdleParam._ 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas de inactividad basadas en el prototipo de [función FNIDLE:](fnidle.md) 
  
|**Función de rutina de inactividad**|**Uso**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad al sistema MAPI, con o sin habilitarlo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Apaga el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de función devuelta por **FtgRegisterIdleRoutine**. 
  
Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse. No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad. 
  


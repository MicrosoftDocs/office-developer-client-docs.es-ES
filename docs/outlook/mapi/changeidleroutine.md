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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1fbeccd805953322b579d1490b5e74e5132aa7ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19816563"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Se aplica a**: Outlook 
  
Cambia algunas o todas las características de una rutina de inactividad [FNIDLE](fnidle.md) en función de. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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

## <a name="parameters"></a>Sintaxis

_ftg_
  
> [entrada] Etiqueta de función que identifica la rutina inactivo. 
    
_pfnIdle_
  
> [entrada] Puntero a la rutina de inactividad. 
    
_pvIdleParam_
  
> [entrada] Puntero a un nuevo bloque de memoria que la implementación de la llamada se asigna para la rutina de inactividad. 
    
_priIdle_
  
> [entrada] Valor que representa una nueva prioridad para la rutina de inactividad. Las posibles prioridades para rutinas definido por la implementación son mayor o menor que cero, pero no es cero. Un valor de cero está reservado para un evento de usuario como un clic del mouse o un mensaje WM_PAINT. Los valores mayores que cero representan las prioridades para tareas en segundo plano que tienen una mayor prioridad a los eventos de usuario y se envían como parte del bucle de suministro de mensajes de Windows estándar. Los valores inferiores a cero representan las prioridades para tareas inactivas que ejecutan sólo durante el tiempo de inactividad de suministro de mensajes. Ejemplos de las prioridades son: 1 para el envío de primer plano, 1 para la inserción de caracteres de edición de energía y 3 para la descarga de los mensajes nuevos.
    
_csecIdle_
  
> [entrada] Una nueva hora, en centésimas de segundo, que se debe aplicar a la rutina de inactividad. El significado del valor inicial de tiempo varía en función de lo que se pasa en el parámetro _iroIdle_ . Puede ser: 
    
  - El período mínimo de omisión de usuario que debe transcurrir antes de la MAPI motor inactivo llama a la rutina de inactividad por primera vez, si se establece la marca FIROWAIT en _iroIdle_. Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
  - El intervalo mínimo entre las llamadas a la rutina de inactividad, si se establece la marca FIROINTERVAL en _iroIdle_. 
    
_iroIdle_
  
> [entrada] Máscara de bits de marcadores que indica nuevas opciones para llamar a la rutina de inactividad. Debe establecerse exactamente uno de los siguientes indicadores:
    
  - FIROINTERVAL: El tiempo especificado por el parámetro _csecIdle_ es el intervalo mínimo entre las llamadas sucesivas a la rutina de inactividad. 
      
  - FIROONCEONLY: obsoleto. No la use. 
      
  - FIROPERBLOCK: obsoleto. No la use. 
      
  - FIROWAIT: El tiempo especificado por el parámetro _csecIdle_ es el período mínimo de omisión de usuario que debe transcurrir antes de que el motor de inactividad de MAPI llama a la rutina de inactividad por primera vez. Una vez transcurrido este tiempo, el motor de inactividad puede llamar a la rutina de inactividad tantas veces como sea necesario. 
    
_ircIdle_
  
> [entrada] Máscara de bits de indicadores que se utilizan para indicar los cambios que hacer en la rutina de inactividad. Las siguientes marcas se pueden establecer en cualquier combinación:
    
  - FIRCCSEC: Un cambio en el tiempo asociado con la rutina de inactividad, es decir, un cambio indicada por el valor que se pasa en el parámetro _csecIdle_ . 
      
  - FIRCIRO: Un cambio en las opciones para la rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _iroIdle_ . 
      
  - FIRCPFN: Un cambio en el puntero de rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _pfnIdle_ . 
      
  - FIRCPRI: Un cambio en la prioridad de la rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _priIdle_ . 
      
  - FIRCPV: Un cambio en el bloque de memoria de la rutina inactivo, es decir, un cambio indicado por el valor que se pasa en el parámetro _pvIdleParam_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Observaciones

Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) : 
  
|**Función rutina inactivo**|**Uso**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Se cierra el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**. 
  
Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar. No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada. 
  


---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85161fb87e798bbb03b267f9760870da1246e48d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816663"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**Hace referencia a**: Outlook 
  
Quita un [FNIDLE](fnidle.md) basa rutina inactivo desde el sistema de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Parámetros

 _ftg_
  
> [entrada] Etiqueta de función que identifica la rutina inactivo que se va a quitar.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Cualquier tarea en una aplicación de cliente o un proveedor de servicios puede anular el registro de cualquier rutina de inactividad para el que tiene un parámetro válido _ftg_ . En concreto, una rutina de inactividad puede anular el registro de sí mismo. 
  
Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) : 
  
|**Función rutina inactivo**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|**DeregisterIdleRoutine** <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Se cierra el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**. 
  
Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar. No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada. 
  
Después de la rutina de inactividad se elimina del registro, el motor de inactividad no llame nuevamente. Cualquier implementación que llama a **DeregisterIdleRoutine** debe desasignar los bloques de memoria a la que se pasan punteros para el motor de inactivo a usar en su llamada original a la función **FtgRegisterIdleRoutine** . 
  


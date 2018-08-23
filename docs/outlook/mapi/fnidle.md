---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbad4b903592f83fc7d72fde21f149c9835f2e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575640"
---
# <a name="fnidle"></a>FNIDLE
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una rutina de inactividad que el motor de inactividad de MAPI llama periódicamente según la prioridad. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Función definido implementada por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
|Llamado por una función definida:  <br/> |MAPI  <br/> |
|Tipo de puntero correspondiente:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parámetros

 _lpvContext_
  
> [entrada] Puntero a un bloque de memoria que MAPI pasadas a la rutina de inactividad cada vez que lo llama. Este puntero se pasa al motor de inactividad de MAPI en el parámetro _pvIdleParam_ por [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Los datos en el bloque de memoria pueden proporcionar contexto para la llamada a la rutina de inactividad, como qué objeto para funcionar en, o el estado actual de una operación larga.
    
## <a name="return-value"></a>Valor devuelto

FALSE 
  
> Una rutina de inactividad con el prototipo **FNIDLE** siempre debe devolver FALSE. 
    
## <a name="remarks"></a>Comentarios

La funcionalidad específica de la rutina de inactividad se determina mediante la implementación de la aplicación de cliente o un proveedor de servicio. 
  
El cliente o el proveedor debe limitar el tiempo de ejecución de cada estado de una rutina de inactividad. Cada estado debe realizar una cantidad mínima de procesamiento, actualizar el estado actual de los datos de contexto que señala _lpvContext_y volver al motor de inactividad de MAPI. 
  
El cliente o el proveedor debe llamar a la función MAPI [MAPIInitIdle](mapiinitidle.md) antes de que se puede registrar su propia rutina de inactividad con una llamada a la función [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) . 
  
Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función FNIDLE: 
  
|**Función rutina inactivo**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Se cierra el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**. 
  
Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar. No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada. 
  


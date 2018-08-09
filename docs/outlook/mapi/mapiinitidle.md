---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e4f4cdd1d0ed2e03d49f471e6e91464b7973c920
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818255"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Hace referencia a**: Outlook 
  
Inicializa el motor de inactividad de MAPI para la aplicación de llamada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parámetros

 _lpvReserved_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

La función **MAPIInitIdle** devuelve cero si la inicialización es correcta y 1, en caso contrario. Si se llama a **MAPIInitIdle** varias veces, todas las llamadas adicionales se realizan con éxito, pero se omiten excepto to incrementar el recuento de referencia. 
  
## <a name="remarks"></a>Comentarios

Una aplicación de cliente o un proveedor de servicios debe llamar a **MAPIInitIdle** antes de llamar a cualquier otra función de motor inactivo. 
  
Todas las llamadas a **MAPIInitIdle** deben coincidir por una llamada a [MAPIDeInitIdle](mapideinitidle.md)posterior o el motor de inactividad quedo en ejecución para la aplicación de llamada. 
  
Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) : 
  
|**Función rutina inactivo**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Se cierra el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
|**MAPIInitIdle** <br/> |Inicializa el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
   
Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar. No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada. 
  


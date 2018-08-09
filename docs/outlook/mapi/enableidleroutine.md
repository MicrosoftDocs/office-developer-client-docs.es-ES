---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00b5c123e588636654fb4287cc7b45500d47d89c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816755"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**Hace referencia a**: Outlook 
  
Habilita o deshabilita una rutina de inactividad en función de [FNIDLE](fnidle.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>Parámetros

 _ftg_
  
> [entrada] Etiqueta de función que identifica la rutina inactivo para que estén habilitadas o deshabilitadas. 
    
 _fEnable_
  
> [entrada] Contiene TRUE si el motor de inactividad debe habilitar la rutina de inactividad o FALSE si debe deshabilitarlo.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las siguientes funciones de abordar los problemas con el motor de inactividad de MAPI y con las rutinas de inactividad según el prototipo de función [FNIDLE](fnidle.md) : 
  
|**Función rutina inactivo**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|**EnableIdleRoutine** <br/> |Deshabilita o habilita volver a una rutina de inactividad registrada sin quitar desde el sistema de MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad en el sistema MAPI, con o sin habilitarla.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Se cierra el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad de MAPI para la aplicación de llamada.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como un parámetro de entrada de la etiqueta de función devuelto por **FtgRegisterIdleRoutine**. 
  
Cuando se convierten en todas las tareas de primer plano de la plataforma de inactividad, el motor de inactividad de MAPI llama a la rutina de inactividad de prioridad más alta que esté lista para ejecutar. No hay ninguna garantía de orden entre las rutinas de inactividad de la misma prioridad de llamada. 
  


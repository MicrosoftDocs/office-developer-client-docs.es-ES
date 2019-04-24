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
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339399"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Habilita o deshabilita una rutina de inactividad basada en [FNIDLE](fnidle.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>Parameters

 _FTG_
  
> a Etiqueta de función que identifica la rutina inactiva que se va a habilitar o deshabilitar. 
    
 _fEnable_
  
> a Contiene TRUE si el motor inactivo debe habilitar la rutina inactiva o FALSE si debe deshabilitarla.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE](fnidle.md) : 
  
|**Función de rutina inActiva**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina inactiva registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina inactiva registrada del sistema MAPI.  <br/> |
|**EnableIdleRoutine** <br/> |Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de la función devuelta por **FtgRegisterIdleRoutine**. 
  
Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse. No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad. 
  


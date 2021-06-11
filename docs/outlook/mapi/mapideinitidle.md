---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408211"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Apaga el motor de inactividad MAPI para la aplicación de llamada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>Parámetros

Ninguno. 
  
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Una aplicación cliente o un proveedor de servicios debe llamar a **MAPIDeInitIdle** cuando ya no necesite el motor inactivo, por ejemplo, cuando está a punto de detener el procesamiento. 
  
Cada llamada a [MAPIInitIdle](mapiinitidle.md) debe coincidir con una llamada posterior a **MAPIDeInitIdle** o el motor inactivo se deja en ejecución para la aplicación de llamada. 
  
Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas de inactividad basadas en el prototipo de [función FNIDLE:](fnidle.md) 
  
|**Función de rutina de inactividad**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad al sistema MAPI, con o sin habilitarlo.  <br/> |
|**MAPIDeInitIdle** <br/> |Apaga el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
   
Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse. No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad. 
  


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
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346658"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parameters

 _lpvReserved_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

La función **MAPIInitIdle** devuelve cero si la inicialización es correcta y 1 en caso contrario. Si se llama a **MAPIInitIdle** varias veces, todas las llamadas adicionales se realizan correctamente, pero se omiten excepto para incrementar el recuento de referencia. 
  
## <a name="remarks"></a>Comentarios

Una aplicación cliente o un proveedor de servicios debe llamar a **MAPIInitIdle** antes de llamar a cualquier otra función del motor de inactividad. 
  
Cada llamada a **MAPIInitIdle** debe coincidir con una llamada subsiguiente a [MAPIDeInitIdle](mapideinitidle.md)o el motor inactivo se deja en ejecución para la aplicación que realiza la llamada. 
  
Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función [FNIDLE](fnidle.md) : 
  
|**Función de rutina inActiva**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina inactiva registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina inactiva registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.  <br/> |
|**MAPIInitIdle** <br/> |Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.  <br/> |
   
Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse. No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad. 
  


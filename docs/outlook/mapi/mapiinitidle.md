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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432446"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicializa el motor de inactividad MAPI para la aplicación de llamada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
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

La **función MAPIInitIdle** devuelve cero si la inicialización se realiza correctamente y 1 en caso contrario. Si **se llama a MAPIInitIdle** varias veces, todas las llamadas adicionales se realiza correctamente, pero se omiten excepto para incrementar el recuento de referencias. 
  
## <a name="remarks"></a>Comentarios

Una aplicación cliente o proveedor de servicios debe llamar **a MAPIInitIdle** antes de llamar a cualquier otra función del motor inactivo. 
  
Cada llamada a **MAPIInitIdle** debe coincidir con una llamada posterior a [MAPIDeInitIdle](mapideinitidle.md)o el motor inactivo se deja en ejecución para la aplicación de llamada. 
  
Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas de inactividad basadas en el prototipo de [función FNIDLE:](fnidle.md) 
  
|**Función de rutina de inactividad**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina de inactividad al sistema MAPI, con o sin habilitarlo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Apaga el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
|**MAPIInitIdle** <br/> |Inicializa el motor de inactividad MAPI para la aplicación de llamada.  <br/> |
   
Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse. No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad. 
  


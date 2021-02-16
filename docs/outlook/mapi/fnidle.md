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
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412383"
---
# <a name="fnidle"></a>FNIDLE
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una rutina inactiva a la que el motor de inactividad MAPI llama periódicamente según la prioridad. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Función definida implementada por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
|Tipo de puntero correspondiente:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parámetros

 _lpvContext_
  
> [entrada] Puntero a un bloque de memoria que MAPI pasa a la rutina inactiva cada vez que lo llama. Este puntero se pasa al motor inactivo MAPI en el parámetro  _pvIdleParam_ [mediante FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Los datos del bloque de memoria pueden proporcionar contexto para la llamada a la rutina inactiva, como el objeto en el que se va a operar o el estado actual de una operación larga.
    
## <a name="return-value"></a>Valor devuelto

FALSE 
  
> Una rutina inactiva con el **prototipo FNIDLE** siempre debe devolver FALSE. 
    
## <a name="remarks"></a>Comentarios

La funcionalidad específica de la rutina inactiva la determina la aplicación cliente o el proveedor de servicios de implementación. 
  
El cliente o proveedor debe limitar el tiempo de ejecución de cada estado de una rutina inactiva. Cada estado debe realizar una cantidad mínima de procesamiento, actualizar el estado actual en los datos de contexto a los que apunta  _lpvContext_ y volver al motor inactivo MAPI. 
  
El cliente o proveedor debe llamar a la función [MAPI MAPIInitIdle](mapiinitidle.md) para poder registrar su propia rutina inactiva con una llamada a la función [FtgRegisterIdleRoutine.](ftgregisteridleroutine.md) 
  
Las siguientes funciones tratan con el motor de inactividad MAPI y con rutinas inactivas basadas en el prototipo de función FNIDLE: 
  
|**Función de rutina inactiva**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina de inactividad registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina de inactividad registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina de inactividad registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina inactiva al sistema MAPI, con o sin habilitarla.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Cierra el motor de inactividad MAPI para la aplicación que realiza la llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación que llama.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de función devuelta por **FtgRegisterIdleRoutine**. 
  
Cuando todas las tareas en primer plano de la plataforma están inactivas, el motor de inactividad MAPI llama a la rutina de inactividad de prioridad más alta que está lista para ejecutarse. No hay ninguna garantía de orden de llamada entre rutinas inactivas de la misma prioridad. 
  


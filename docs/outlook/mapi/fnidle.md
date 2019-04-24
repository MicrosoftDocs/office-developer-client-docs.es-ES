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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342248"
---
# <a name="fnidle"></a>FNIDLE
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una rutina inactiva que el motor de inactividad de MAPI llama periódicamente de acuerdo con la prioridad. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Función definida implementada por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
|Tipo de puntero correspondiente:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameters

 _lpvContext_
  
> a Puntero a un bloque de memoria que MAPI pasa a la rutina inactiva cada vez que lo llama. Este puntero se pasa al motor de inactividad MAPI en el parámetro _pvIdleParam_ por [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Los datos en el bloque de memoria pueden proporcionar contexto para la llamada a la rutina inactiva, como el objeto en el que operar o el estado actual de una operación prolongada.
    
## <a name="return-value"></a>Valor devuelto

FALSE 
  
> Una rutina inactiva con el prototipo **FNIDLE** siempre debe devolver false. 
    
## <a name="remarks"></a>Comentarios

La funcionalidad específica de la rutina inactiva está determinada por el proveedor de servicios o la aplicación cliente que se está implementando. 
  
El cliente o el proveedor debe limitar el tiempo de ejecución de cada estado de una rutina inactiva. Cada Estado debe realizar una cantidad mínima de procesamiento, actualizar el estado actual en los datos de contexto señalados por _lpvContext_y volver al motor de inACTIVIDAD de MAPI. 
  
El cliente o el proveedor debe llamar a la función MAPI [MAPIInitIdle](mapiinitidle.md) antes de que pueda registrar su propia rutina inactiva con una llamada a la función [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) . 
  
Las siguientes funciones tratan con el motor de inactividad de MAPI y con rutinas inactivas basadas en el prototipo de función FNIDLE: 
  
|**Función de rutina inActiva**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Cambia las características de una rutina inactiva registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Quita una rutina inactiva registrada del sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deshabilita o vuelve a habilitar una rutina inactiva registrada sin quitarla del sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Agrega una rutina inactiva al sistema MAPI, con o sin habilitar.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Cierra el motor de inactividad MAPI de la aplicación que realiza la llamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa el motor de inactividad MAPI para la aplicación que realiza la llamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**y **EnableIdleRoutine** toman como parámetro de entrada la etiqueta de la función devuelta por **FtgRegisterIdleRoutine**. 
  
Cuando todas las tareas de primer plano de la plataforma se convierten en inactivas, el motor de inactividad de MAPI llama a la rutina inactiva de máxima prioridad que está lista para ejecutarse. No hay ninguna garantía del orden de llamadas entre rutinas de inactividad de la misma prioridad. 
  


---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573190"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada que puede liberar una interfaz **IStorage** después de la versión final de un objeto **IMessage** fundamentan con la función [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage.h  <br/> |
|Función definido implementada por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
|Llamado por una función definida:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parámetros

 _ulCallerData_
  
> [entrada] Contiene información de la aplicación que llama acerca de **la interfaz** . 
    
 _lpMessage_
  
> [entrada] Puntero para el mensaje de nivel superior y los datos adjuntos que se han publicado.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  


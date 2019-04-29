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
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405915"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada que puede liberar una interfaz **IStorage** después de la versión final de un objeto **IMessage** creado encima de ella con la función [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage. h  <br/> |
|Función definida implementada por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parameters

 _ulCallerData_
  
> a Contiene información de la aplicación de llamada sobre la interfaz **IMessage** . 
    
 _lpMessage_
  
> a Puntero al mensaje de nivel superior y datos adjuntos que se han lanzado.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  


---
title: Sección de MapiSvc.inf [asignaciones de archivo de ayuda]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 776f797d0c96d9173e114fd499d6cca0494a0a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818288"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Sección de MapiSvc.inf [asignaciones de archivo de ayuda]

  
  
**Se aplica a**: Outlook 
  
La sección **[Help File Mappings]** contiene entradas que cada uno de ellos se asignan un servicio de mensajes al archivo que se proporciona ayuda para los errores generados por el servicio. Las entradas de esta sección use el siguiente formato: 
  
 **[Asignaciones de archivo de ayuda]** _nombre de servicio de mensajes_  =   _Nombre de archivo de ayuda_
  
El nombre del servicio de mensajes es el nombre del servicio de mensajes instalado; el nombre de archivo de ayuda es el nombre del archivo en el que reside la información de error. El siguiente ejemplo muestra una sección típica **[Help File Mappings]** que contiene entradas para tres servicios: MAPI, el servicio de MsgService y el servicio de MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```



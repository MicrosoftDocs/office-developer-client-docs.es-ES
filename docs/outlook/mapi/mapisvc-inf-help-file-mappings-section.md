---
title: Sección MapiSvc. inf [asignaciones de archivo de ayuda]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269975"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Sección MapiSvc. inf [asignaciones de archivo de ayuda]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Help File mappings]** contiene entradas que asignan un servicio de mensajes al archivo que proporciona ayuda para los errores generados por el servicio. Las entradas de esta sección usan el siguiente formato: 
  
 **[Asignaciones de archivo de ayuda]** _nombre del servicio de mensajes_  =   _Nombre de archivo de ayuda_
  
El nombre del servicio de mensajes es el nombre del servicio de mensajes instalado; el nombre del archivo de ayuda es el nombre del archivo donde reside la información del error. En el ejemplo siguiente se muestra una sección **[file mappings de la ayuda]** típica que contiene entradas para tres servicios: MAPI, el servicio MsgService y el servicio MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```



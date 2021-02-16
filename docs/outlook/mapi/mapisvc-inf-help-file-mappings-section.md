---
title: Sección MapiSvc.inf [Asignaciones de archivo de Ayuda]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407560"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Sección MapiSvc.inf [Asignaciones de archivos de Ayuda]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **sección [Asignaciones de** archivos de ayuda] contiene entradas que cada servicio de mensajes asigna al archivo que proporciona ayuda para los errores generados por el servicio. Las entradas de esta sección tienen el siguiente formato: 
  
 **Nombre del archivo de ayuda del nombre** del servicio de _mensaje_[Asignaciones de archivo  =   _de ayuda]_
  
El nombre del servicio de mensajes es el nombre del servicio de mensajes instalado; El nombre del archivo de ayuda es el nombre del archivo donde reside la información de error. En el siguiente ejemplo se muestra una sección **típica [Asignaciones** de archivo de Ayuda] que contiene entradas para tres servicios: MAPI, el servicio MsgService y el servicio MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```



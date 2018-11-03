---
title: Cómo registrar los objetos de negocios en el cliente para usan con DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2746ad6d0736f4415788cde477e1513d9b46146
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946807"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Cómo registrar los objetos de negocios en el cliente para usan con DCOM

**Se aplica a**: Access 2013, Office 2013

Los objetos de negocio personalizados necesitan garantizar que la parte del cliente pueda hacer corresponder su nombre de programa (ProgId) con un identificador (CLSID) que se pueda usar con DCOM. Por ello, el ProgID del objeto DCOM debe estar en el Registro del cliente y asociado al identificador de clase del objeto de negocio de la parte del servidor. Para los demás protocolos admitidos (HTTP, HTTPS y en proceso), esto no es necesario.

Por ejemplo, si expone un objeto de negocio del servidor, llamado MyBObj, con un ID de clase específico, por ejemplo "{00112233-4455-6677-8899-00AABBCCDDEE\", asegúrese de que las entradas siguientes se agregan al Registro del cliente:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```


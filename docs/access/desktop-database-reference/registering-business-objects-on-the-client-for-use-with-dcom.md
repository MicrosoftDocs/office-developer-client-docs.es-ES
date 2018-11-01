---
title: Registrar objetos de negocio en el cliente para su uso con DCOM
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b106fa88df8205595312aaebdabf82cf12d57c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887813"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Registrar objetos de negocio en el cliente para su uso con DCOM


**Se aplica a**: Access 2013, Office 2013

Los objetos de negocio personalizados necesitan garantizar que la parte del cliente pueda hacer corresponder su nombre de programa (ProgId) con un identificador (CLSID) que se pueda usar con DCOM. Por ello, el ProgID del objeto DCOM debe estar en el Registro del cliente y asociado al identificador de clase del objeto de negocio de la parte del servidor. Para los demás protocolos admitidos (HTTP, HTTPS y en proceso), esto no es necesario.

Por ejemplo, si expone un objeto de negocio del servidor, llamado MyBObj, con un ID de clase específico, por ejemplo "{00112233-4455-6677-8899-00AABBCCDDEE\", asegúrese de que las entradas siguientes se agregan al Registro del cliente:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```


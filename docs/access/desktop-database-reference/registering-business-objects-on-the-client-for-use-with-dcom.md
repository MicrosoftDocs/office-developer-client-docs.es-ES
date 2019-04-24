---
title: Registro de objetos de negocio en el cliente para el uso con DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7479eefcc975ca0fe7bb7fe0d51796d1b1f416b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307124"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Registro de objetos de negocio en el cliente para el uso con DCOM

**Se aplica a:** Access 2013, Office 2013

Los objetos de negocio personalizados necesitan garantizar que la parte del cliente pueda hacer corresponder su nombre de programa (ProgId) con un identificador (CLSID) que se pueda usar con DCOM. Por ello, el ProgID del objeto DCOM debe estar en el Registro del cliente y asociado al identificador de clase del objeto de negocio de la parte del servidor. Para los demás protocolos admitidos (HTTP, HTTPS y en proceso), esto no es necesario.

For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```


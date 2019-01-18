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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705515"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="f6a04-102">Registro de objetos de negocio en el cliente para el uso con DCOM</span><span class="sxs-lookup"><span data-stu-id="f6a04-102">Registering business objects on the client for use with DCOM</span></span>

<span data-ttu-id="f6a04-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6a04-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6a04-p101">Los objetos de negocio personalizados necesitan garantizar que la parte del cliente pueda hacer corresponder su nombre de programa (ProgId) con un identificador (CLSID) que se pueda usar con DCOM. Por ello, el ProgID del objeto DCOM debe estar en el Registro del cliente y asociado al identificador de clase del objeto de negocio de la parte del servidor. Para los demás protocolos admitidos (HTTP, HTTPS y en proceso), esto no es necesario.</span><span class="sxs-lookup"><span data-stu-id="f6a04-p101">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM. For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object. For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="f6a04-107">Por ejemplo, si expone un objeto de negocio del servidor, llamado MyBObj, con un ID de clase específico, por ejemplo "{00112233-4455-6677-8899-00AABBCCDDEE\", asegúrese de que las entradas siguientes se agregan al Registro del cliente:</span><span class="sxs-lookup"><span data-stu-id="f6a04-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```


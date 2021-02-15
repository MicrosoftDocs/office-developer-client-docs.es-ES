---
title: Emisión de comandos al proveedor de datos subyacente
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291091"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="e0073-102">Emisión de comandos al proveedor de datos subyacente</span><span class="sxs-lookup"><span data-stu-id="e0073-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="e0073-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0073-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0073-p101">Cualquier comando que no empiece por SHAPE se pasa al proveedor de datos. Esto equivale a emitir un comando Shape de la forma "SHAPE {comando de proveedor}". Estos comandos *no* tienen que producir un **conjunto de registros**. Por ejemplo, "SHAPE {DROP TABLE MyTable} es un comando Shape perfectamente válido, suponiendo que el proveedor de datos admite DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="e0073-p101">Any command that does not begin with SHAPE is passed through to the data provider. This is equivalent to issuing a shape command in the form "SHAPE {provider command}". These commands do *not* have to produce a **Recordset**. For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="e0073-108">Esta característica permite que los comandos de proveedor normal y los comandos Shape compartan la misma conexión y la misma transacción.</span><span class="sxs-lookup"><span data-stu-id="e0073-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>


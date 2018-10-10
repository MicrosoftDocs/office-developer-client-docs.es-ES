---
title: Emitir comandos al proveedor de datos subyacente
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484411"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="966f4-102">Emitir comandos al proveedor de datos subyacente</span><span class="sxs-lookup"><span data-stu-id="966f4-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="966f4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="966f4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="966f4-104">Cualquier comando que no empiece por SHAPE se pasa al proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="966f4-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="966f4-105">Esto equivale a emitir un comando Shape de la forma "SHAPE {comando de proveedor}".</span><span class="sxs-lookup"><span data-stu-id="966f4-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="966f4-106">Estos comandos *no* tienen que producir un **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="966f4-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="966f4-107">Por ejemplo, "SHAPE {DROP TABLE MyTable} es un comando Shape perfectamente válido, suponiendo que el proveedor de datos admite DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="966f4-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="966f4-108">Esta característica permite que los comandos de proveedor normal y los comandos Shape compartan la misma conexión y la misma transacción.</span><span class="sxs-lookup"><span data-stu-id="966f4-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>


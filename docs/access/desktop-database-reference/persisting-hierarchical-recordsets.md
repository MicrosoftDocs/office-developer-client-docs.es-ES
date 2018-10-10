---
title: Almacenar conjuntos de registros jerárquicos
TOCTitle: Persisting Hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36c6c1d99b01918d848dfde06c26ad6851b1db43
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485134"
---
# <a name="persisting-hierarchical-recordsets"></a><span data-ttu-id="98861-102">Almacenar conjuntos de registros jerárquicos</span><span class="sxs-lookup"><span data-stu-id="98861-102">Persisting Hierarchical Recordsets</span></span>


<span data-ttu-id="98861-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98861-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98861-p101">Puede guardar un objeto **Recordset** jerárquico en un archivo, en formato ADTG o XML, llamando al método [Save](save-method-ado.md). Sin embargo, se aplican dos limitaciones cuando se guardan objetos **Recordset** jerárquicos en formato XML: no se puede guardar en XML si el objeto **Recordset** jerárquico contiene actualizaciones pendientes y no se puede guardar un objeto **Recordset** jerárquico parametrizado.</span><span class="sxs-lookup"><span data-stu-id="98861-p101">You can save a hierarchical **Recordset** to a file in either ADTG or XML format by calling the [Save](save-method-ado.md) method. However, two limitations apply when saving hierarchical **Recordset**s in XML format: You cannot save in XML if the hierarchical **Recordset** contains pending updates, and you cannot save a parameterized hierarchical **Recordset**.</span></span>

<span data-ttu-id="98861-106">Para obtener más información sobre el proveedor para forma de datos, vea [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) y el Servicio de forma de datos para OLE DB (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="98861-106">For more information about the Data Shaping provider, see [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) and The Data Shaping Service for OLE DB(OLE DB).</span></span>


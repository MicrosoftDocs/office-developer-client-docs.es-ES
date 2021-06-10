---
title: Colección Indexes (ADOX)
TOCTitle: Indexes collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6eac0d1b73e0380f582ce0bc69cdb358c67d185e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291583"
---
# <a name="indexes-collection-adox"></a><span data-ttu-id="c1835-102">Colección Indexes (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c1835-102">Indexes collection (ADOX)</span></span>


<span data-ttu-id="c1835-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1835-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1835-104">Contiene todos los objetos [Index](index-object-adox.md) de una tabla.</span><span class="sxs-lookup"><span data-stu-id="c1835-104">Contains all [Index](index-object-adox.md) objects of a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1835-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1835-105">Remarks</span></span>

<span data-ttu-id="c1835-p101">El método [Append](append-method-adox-indexes.md) de una colección **Indexes** es único para ADOX. Se puede:</span><span class="sxs-lookup"><span data-stu-id="c1835-p101">The [Append](append-method-adox-indexes.md) method for an **Indexes** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="c1835-108">Agregar un nuevo índice a la colección con el método **Append**.</span><span class="sxs-lookup"><span data-stu-id="c1835-108">Add a new index to the collection with the **Append** method.</span></span>

<span data-ttu-id="c1835-p102">Los demás métodos y propiedades son estándar en las colecciones ADO. Se puede:</span><span class="sxs-lookup"><span data-stu-id="c1835-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="c1835-111">Tener acceso a un índice de la colección con la propiedad [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1835-111">Access an index in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="c1835-112">Devolver el número de índices incluido en la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1835-112">Return the number of indexes contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="c1835-113">Quitar un índice de la colección con el método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="c1835-113">Remove an index from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="c1835-114">Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1835-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


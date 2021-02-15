---
title: Colección Columns (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1827fe11696e28871bdd03594ff0d7057c377dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296209"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="ce681-102">Colección Columns (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ce681-102">Columns collection (ADOX)</span></span>


<span data-ttu-id="ce681-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce681-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce681-104">Contiene todos los objetos [Column](column-object-adox.md) de una tabla, un índice o una clave.</span><span class="sxs-lookup"><span data-stu-id="ce681-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce681-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce681-105">Remarks</span></span>

<span data-ttu-id="ce681-p101">El método [Append](append-method-adox-columns.md) de una colección **Columns** es único para ADOX. Se puede:</span><span class="sxs-lookup"><span data-stu-id="ce681-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="ce681-108">Agregar una nueva columna a la colección con el método **Append**.</span><span class="sxs-lookup"><span data-stu-id="ce681-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="ce681-p102">Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:</span><span class="sxs-lookup"><span data-stu-id="ce681-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="ce681-111">Tener acceso a una columna de la colección con la propiedad [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ce681-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="ce681-112">Devolver el número de columnas incluido en la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ce681-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="ce681-113">Quitar una columna de la colección con el método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="ce681-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="ce681-114">Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ce681-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="ce681-115">[!NOTA] Si se anexa una **columna** a la colección **Columns** de un [índice](index-object-adox.md) pero la **columna** no existe en alguna [tabla](table-object-adox.md) que ya se haya anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="ce681-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>



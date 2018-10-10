---
title: Columns (colección) (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486144"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="44c55-102">Columns (colección) (ADOX)</span><span class="sxs-lookup"><span data-stu-id="44c55-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="44c55-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="44c55-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="44c55-104">Contiene todos los objetos [Column](column-object-adox.md) de una tabla, un índice o una clave.</span><span class="sxs-lookup"><span data-stu-id="44c55-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="44c55-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44c55-105">Remarks</span></span>

<span data-ttu-id="44c55-p101">El método [Append](append-method-adox-columns.md) de una colección **Columns** es único para ADOX. Se puede:</span><span class="sxs-lookup"><span data-stu-id="44c55-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="44c55-108">Agregar una nueva columna a la colección con el método **Append**.</span><span class="sxs-lookup"><span data-stu-id="44c55-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="44c55-p102">Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:</span><span class="sxs-lookup"><span data-stu-id="44c55-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="44c55-111">Tener acceso a una columna de la colección con la propiedad [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="44c55-112">Devolver el número de columnas incluido en la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="44c55-113">Quitar una columna de la colección con el método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="44c55-114">Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="44c55-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="44c55-115">[!NOTA] Si se anexa una <STRONG>columna</STRONG> a la colección <STRONG>Columns</STRONG> de un <A href="index-object-adox.md">índice</A> pero la <STRONG>columna</STRONG> no existe en alguna <A href="table-object-adox.md">tabla</A> que ya se haya anexado a la colección <A href="tables-collection-adox.md">Tables</A>, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="44c55-115">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>



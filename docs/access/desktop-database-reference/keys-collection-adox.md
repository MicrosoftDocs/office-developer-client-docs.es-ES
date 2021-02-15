---
title: Colección Keys (ADOX)
TOCTitle: Keys collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43e6643e585ed8c28cd710e0674523b84d12d89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290253"
---
# <a name="keys-collection-adox"></a><span data-ttu-id="454da-102">Colección Keys (ADOX)</span><span class="sxs-lookup"><span data-stu-id="454da-102">Keys collection (ADOX)</span></span>


<span data-ttu-id="454da-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="454da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="454da-104">Contiene todos los objetos [Key](key-object-adox.md) de una tabla.</span><span class="sxs-lookup"><span data-stu-id="454da-104">Contains all [Key](key-object-adox.md) objects of a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="454da-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="454da-105">Remarks</span></span>

<span data-ttu-id="454da-p101">El método [Append](append-method-adox-keys.md) de una colección **Keys** es único para ADOX. Se puede:</span><span class="sxs-lookup"><span data-stu-id="454da-p101">The [Append](append-method-adox-keys.md) method for a **Keys** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="454da-108">Agregar una nueva clave a la colección con el método **Append**.</span><span class="sxs-lookup"><span data-stu-id="454da-108">Add a new key to the collection with the **Append** method.</span></span>

<span data-ttu-id="454da-p102">Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:</span><span class="sxs-lookup"><span data-stu-id="454da-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="454da-111">Tener acceso a una clave de la colección con la propiedad [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="454da-111">Access a key in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="454da-112">Devolver el número de claves incluido en la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="454da-112">Return the number of keys contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="454da-113">Quitar una clave de la colección con el método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="454da-113">Remove a key from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="454da-114">Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="454da-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


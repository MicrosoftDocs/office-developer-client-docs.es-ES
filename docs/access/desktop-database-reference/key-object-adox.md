---
title: Objeto Key (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7722130c76516eaa7dcaf0598a5e1c040e21ba25
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025948"
---
# <a name="key-object-adox"></a><span data-ttu-id="d643c-102">Key (objeto, ADOX)</span><span class="sxs-lookup"><span data-stu-id="d643c-102">Key object (ADOX)</span></span>


<span data-ttu-id="d643c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d643c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d643c-104">Representa un campo de clave principal, externa o única de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d643c-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="d643c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d643c-105">Remarks</span></span>

<span data-ttu-id="d643c-106">El siguiente código crea un nuevo objeto **Key**:</span><span class="sxs-lookup"><span data-stu-id="d643c-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="d643c-107">Con las propiedades y las colecciones de un objeto **Key**, se puede:</span><span class="sxs-lookup"><span data-stu-id="d643c-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="d643c-108">Identificar la clave con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d643c-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="d643c-109">Determinar si la clave es principal, externa o única con la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).</span><span class="sxs-lookup"><span data-stu-id="d643c-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="d643c-110">Tener acceso a las columnas de base de datos de la clave con la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d643c-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="d643c-111">Especificar el nombre de la tabla relacionada con la propiedad [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d643c-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="d643c-112">Determinar la acción realizada al eliminar o actualizar una clave principal con las propiedades [DeleteRule](deleterule-property-adox.md) y [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d643c-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>


---
title: Objeto Key (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11bd05c4959ba1f3e1819e482ce311fc798bf0e6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929835"
---
# <a name="key-object-adox"></a><span data-ttu-id="80a08-102">Key (objeto, ADOX)</span><span class="sxs-lookup"><span data-stu-id="80a08-102">Key object (ADOX)</span></span>


<span data-ttu-id="80a08-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80a08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80a08-104">Representa un campo de clave principal, externa o única de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="80a08-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="80a08-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80a08-105">Remarks</span></span>

<span data-ttu-id="80a08-106">El siguiente código crea un nuevo objeto **Key**:</span><span class="sxs-lookup"><span data-stu-id="80a08-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="80a08-107">Con las propiedades y las colecciones de un objeto **Key**, se puede:</span><span class="sxs-lookup"><span data-stu-id="80a08-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="80a08-108">Identificar la clave con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="80a08-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="80a08-109">Determinar si la clave es principal, externa o única con la propiedad [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="80a08-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="80a08-110">Tener acceso a las columnas de base de datos de la clave con la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="80a08-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="80a08-111">Especificar el nombre de la tabla relacionada con la propiedad [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="80a08-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="80a08-112">Determinar la acción realizada al eliminar o actualizar una clave principal con las propiedades [DeleteRule](deleterule-property-adox.md) y [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="80a08-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>


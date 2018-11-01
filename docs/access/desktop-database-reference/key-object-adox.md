---
title: Objeto Key (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2edda6dfe7dd9ec28f3eb4cb11714d59806c80e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871363"
---
# <a name="key-object-adox"></a><span data-ttu-id="22d46-102">Key (objeto) (ADOX)</span><span class="sxs-lookup"><span data-stu-id="22d46-102">Key Object (ADOX)</span></span>


<span data-ttu-id="22d46-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22d46-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22d46-104">Representa un campo de clave principal, externa o única de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="22d46-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d46-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22d46-105">Remarks</span></span>

<span data-ttu-id="22d46-106">El siguiente código crea un nuevo objeto **Key**:</span><span class="sxs-lookup"><span data-stu-id="22d46-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="22d46-107">Con las propiedades y las colecciones de un objeto **Key**, se puede:</span><span class="sxs-lookup"><span data-stu-id="22d46-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="22d46-108">Identificar la clave con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="22d46-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="22d46-109">Determinar si la clave es principal, externa o única con la propiedad [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="22d46-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="22d46-110">Tener acceso a las columnas de base de datos de la clave con la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="22d46-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="22d46-111">Especificar el nombre de la tabla relacionada con la propiedad [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="22d46-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="22d46-112">Determinar la acción realizada al eliminar o actualizar una clave principal con las propiedades [DeleteRule](deleterule-property-adox.md) y [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="22d46-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>


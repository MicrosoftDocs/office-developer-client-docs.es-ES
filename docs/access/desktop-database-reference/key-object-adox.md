---
title: 'Objeto Key (ADOX: referencia de base de datos de escritorio de Access)'
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290755"
---
# <a name="key-object-adox"></a><span data-ttu-id="4e245-102">Objeto Key (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4e245-102">Key object (ADOX)</span></span>


<span data-ttu-id="4e245-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e245-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e245-104">Representa un campo de clave principal, externa o única de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4e245-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e245-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e245-105">Remarks</span></span>

<span data-ttu-id="4e245-106">El siguiente código crea un nuevo objeto **Key**:</span><span class="sxs-lookup"><span data-stu-id="4e245-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="4e245-107">Con las propiedades y las colecciones de un objeto **Key**, se puede:</span><span class="sxs-lookup"><span data-stu-id="4e245-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="4e245-108">Identificar la clave con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4e245-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="4e245-109">Determinar si la clave es principal, externa o única con la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).</span><span class="sxs-lookup"><span data-stu-id="4e245-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="4e245-110">Tener acceso a las columnas de base de datos de la clave con la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4e245-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="4e245-111">Especificar el nombre de la tabla relacionada con la propiedad [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4e245-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="4e245-112">Determinar la acción realizada al eliminar o actualizar una clave principal con las propiedades [DeleteRule](deleterule-property-adox.md) y [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4e245-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>


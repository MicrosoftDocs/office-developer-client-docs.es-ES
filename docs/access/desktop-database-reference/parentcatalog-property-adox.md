---
title: ParentCatalog (propiedad, ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287786"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="d6f09-102">ParentCatalog (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="d6f09-102">ParentCatalog property (ADOX)</span></span>


<span data-ttu-id="d6f09-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6f09-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6f09-104">Especifica el catálogo principal de una tabla o una columna para proporcionar acceso a propiedades específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d6f09-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d6f09-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="d6f09-105">Settings and return values</span></span>

<span data-ttu-id="d6f09-p101">Establece y devuelve un objeto [Catalog](catalog-object-adox.md). El establecimiento de **ParentCatalog** en un **catálogo** abierto permite el acceso a propiedades específicas del proveedor antes de anexar una tabla o una columna a una colección **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="d6f09-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f09-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6f09-108">Remarks</span></span>

<span data-ttu-id="d6f09-p102">Algunos proveedores de datos permiten la escritura de valores de propiedades específicas del proveedor solo durante la creación (cuando se anexa una tabla o una columna a su colección **Catalog** ). Para tener acceso a estas propiedades antes de anexar estos objetos a un **catálogo**, primero especifique el **catálogo** en la propiedad **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="d6f09-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="d6f09-111">Si la tabla o la columna se anexa a un **catálogo** distinto del **ParentCatalog**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d6f09-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


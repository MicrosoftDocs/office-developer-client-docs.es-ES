---
title: ParentCatalog (propiedad, ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 644312ab6b51b1b084d2d11f52117cece7afdf0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483831"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="6c846-102">ParentCatalog (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="6c846-102">ParentCatalog Property (ADOX)</span></span>


<span data-ttu-id="6c846-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c846-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6c846-104">Especifica el catálogo principal de una tabla o una columna para proporcionar acceso a propiedades específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6c846-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6c846-105">Configuraciones y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6c846-105">Settings and Return Values</span></span>

<span data-ttu-id="6c846-p101">Establece y devuelve un objeto [Catalog](catalog-object-adox.md). El establecimiento de **ParentCatalog** en un **catálogo** abierto permite el acceso a propiedades específicas del proveedor antes de anexar una tabla o una columna a una colección **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="6c846-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c846-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c846-108">Remarks</span></span>

<span data-ttu-id="6c846-p102">Algunos proveedores de datos permiten la escritura de valores de propiedades específicas del proveedor solo durante la creación (cuando se anexa una tabla o una columna a su colección **Catalog** ). Para tener acceso a estas propiedades antes de anexar estos objetos a un **catálogo**, primero especifique el **catálogo** en la propiedad **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="6c846-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="6c846-111">Si la tabla o la columna se anexa a un **catálogo** distinto del **ParentCatalog**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="6c846-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


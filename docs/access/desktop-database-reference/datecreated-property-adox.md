---
title: DateCreated (propiedad, ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 962c5e00eee3c58d2c02040869fdf1cb454af538
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485692"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="c6ad2-102">DateCreated (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="c6ad2-102">DateCreated Property (ADOX)</span></span>


<span data-ttu-id="c6ad2-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6ad2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6ad2-104">Indica la fecha en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="c6ad2-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6ad2-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c6ad2-105">Return Values</span></span>

<span data-ttu-id="c6ad2-p101">Devuelve un valor **Variant** que especifica la fecha de creación. El valor es nulo si **DateCreated** no es compatible con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="c6ad2-p101">Returns a **Variant** value specifying the date created. The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ad2-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6ad2-108">Remarks</span></span>

<span data-ttu-id="c6ad2-p102">La propiedad **DateCreated** tiene un valor nulo para objetos recién anexados. Después de anexar una nueva [vista](view-object-adox.md) o un [procedimiento](procedure-object-adox.md), debe llamar al método [Refresh](refresh-method-ado.md) de la colección [Views](views-collection-adox.md) o [Procedures](procedures-collection-adox.md) para obtener valores para la propiedad **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="c6ad2-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>


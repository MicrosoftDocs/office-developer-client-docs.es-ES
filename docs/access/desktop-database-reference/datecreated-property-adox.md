---
title: Propiedad DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294424"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="1f380-102">Propiedad DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1f380-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="1f380-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f380-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f380-104">Indica la fecha en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1f380-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f380-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="1f380-105">Return values</span></span>

<span data-ttu-id="1f380-106">Devuelve un valor **Variant** que especifica la fecha de creación.</span><span class="sxs-lookup"><span data-stu-id="1f380-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="1f380-107">El valor es nulo si **DateCreated** no es compatible con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1f380-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f380-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f380-108">Remarks</span></span>

<span data-ttu-id="1f380-p102">La propiedad **DateCreated** tiene un valor nulo para objetos recién anexados. Después de anexar una nueva [vista](view-object-adox.md) o un [procedimiento](procedure-object-adox.md), debe llamar al método [Refresh](refresh-method-ado.md) de la colección [Views](views-collection-adox.md) o [Procedures](procedures-collection-adox.md) para obtener valores para la propiedad **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="1f380-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>


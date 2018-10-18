---
title: DateModified (propiedad, ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceafd13b33536a77a1d793e7167fe8042609be5e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603332"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="0458e-102">DateModified (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="0458e-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="0458e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0458e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0458e-104">Indica la fecha en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="0458e-104">Indicates the date the object was last modified.</span></span>

<span data-ttu-id="0458e-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0458e-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="0458e-106">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0458e-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="0458e-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0458e-107">Return values</span></span>
>>>>>>> <span data-ttu-id="0458e-108">master</span><span class="sxs-lookup"><span data-stu-id="0458e-108">master</span></span>

<span data-ttu-id="0458e-p101">Devuelve un valor **Variant** que especifica la fecha de modificación. El valor es nulo si **DateModified** no es compatible con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0458e-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="0458e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0458e-111">Remarks</span></span>

<span data-ttu-id="0458e-p102">La propiedad **DateModified** tiene un valor nulo para objetos recién anexados. Después de anexar una nueva [vista](view-object-adox.md) o un [procedimiento](procedure-object-adox.md), debe llamar al método [Refresh](refresh-method-ado.md) de la colección [Views](views-collection-adox.md) o [Procedures](procedures-collection-adox.md) para obtener valores para la propiedad **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="0458e-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>


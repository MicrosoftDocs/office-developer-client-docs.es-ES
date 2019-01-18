---
title: NumericScale (propiedad, ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709057"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="43fb1-102">NumericScale (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="43fb1-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="43fb1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43fb1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43fb1-104">Indica la escala de un valor numérico de la columna.</span><span class="sxs-lookup"><span data-stu-id="43fb1-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="43fb1-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="43fb1-105">Settings and return values</span></span>

<span data-ttu-id="43fb1-p101">Establece y devuelve un valor **Byte** que es la escala de valores de datos de la columna cuando la propiedad [Tipo](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) es **adNumeric** o **adDecimal**. **NumericScale** se omite para todos los demás tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="43fb1-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="43fb1-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43fb1-108">Remarks</span></span>

<span data-ttu-id="43fb1-109">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="43fb1-109">The default value is zero (0).</span></span>

<span data-ttu-id="43fb1-110">**NumericScale** es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="43fb1-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>


---
title: NumericScale (propiedad, ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7dd53830216c302d68adf44e1bea88bbc52e980
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921316"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="2d797-102">NumericScale (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="2d797-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="2d797-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d797-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d797-104">Indica la escala de un valor numérico de la columna.</span><span class="sxs-lookup"><span data-stu-id="2d797-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2d797-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="2d797-105">Settings and return values</span></span>

<span data-ttu-id="2d797-p101">Establece y devuelve un valor **Byte** que es la escala de valores de datos de la columna cuando la propiedad [Tipo](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) es **adNumeric** o **adDecimal**. **NumericScale** se omite para todos los demás tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="2d797-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d797-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d797-108">Remarks</span></span>

<span data-ttu-id="2d797-109">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="2d797-109">The default value is zero (0).</span></span>

<span data-ttu-id="2d797-110">**NumericScale** es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="2d797-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>


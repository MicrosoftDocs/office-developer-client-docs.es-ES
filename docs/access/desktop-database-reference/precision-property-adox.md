---
title: Precision (propiedad, ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e64a7166b73c5fca1fa7f5e0b63fabeec715c52
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927504"
---
# <a name="precision-property-adox"></a><span data-ttu-id="4b666-102">Precision (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="4b666-102">Precision property (ADOX)</span></span>


<span data-ttu-id="4b666-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b666-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b666-104">Indica la precisión máxima de los valores de datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="4b666-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4b666-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4b666-105">Settings and return values</span></span>

<span data-ttu-id="4b666-p101">Establece y devuelve un valor **Long** que es la precisión máxima de valores de datos de la columna cuando la propiedad [Tipo](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) es un tipo numérico. **Precision** se omite para todos los demás tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="4b666-p101">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is a numeric type. **Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b666-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b666-108">Remarks</span></span>

<span data-ttu-id="4b666-109">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="4b666-109">The default value is zero (0).</span></span>

<span data-ttu-id="4b666-110">Esta propiedad es de sólo lectura para objetos [Column](column-object-adox.md) ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="4b666-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>


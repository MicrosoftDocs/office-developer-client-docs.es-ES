---
title: Type (propiedad, Stream de ADO)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fdf3f40565f41a3d34b2202c4e079839af1f1ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602744"
---
# <a name="type-property-ado-stream"></a><span data-ttu-id="62c20-102">Type (propiedad, Stream de ADO)</span><span class="sxs-lookup"><span data-stu-id="62c20-102">Type Property (ADO Stream)</span></span>


<span data-ttu-id="62c20-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="62c20-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62c20-104">Indica el tipo de tipo de datos incluidos en el objeto [Stream](stream-object-ado.md) (binarios o texto).</span><span class="sxs-lookup"><span data-stu-id="62c20-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

<span data-ttu-id="62c20-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="62c20-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="62c20-106">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="62c20-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="62c20-107">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="62c20-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="62c20-108">master</span><span class="sxs-lookup"><span data-stu-id="62c20-108">master</span></span>

<span data-ttu-id="62c20-p101">Establece o devuelve un valor [StreamTypeEnum](streamtypeenum.md) que especifica el tipo de datos incluidos en el objeto **Stream**. El valor predeterminado es **adTypeText**. No obstante, si se escriben datos binarios en un nuevo objeto **Stream** vacío, la propiedad **Type** cambiará a **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="62c20-p101">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object. The default value is **adTypeText**. However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c20-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62c20-112">Remarks</span></span>

<span data-ttu-id="62c20-113">La propiedad **Type** es de lectura y escritura únicamente cuando la posición actual se encuentra al inicio del objeto **Stream** ([Position](position-property-ado.md) es 0) y de sólo lectura en todas las demás posiciones.</span><span class="sxs-lookup"><span data-stu-id="62c20-113">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="62c20-p102">La propiedad **Type** determina los métodos que se deben utilizar para leer y escribir el objeto **Stream**. En los objetos **Stream** de texto, utilice [ReadText](readtext-method-ado.md) y [WriteText](writetext-method-ado.md). En los objetos **Stream** binarios, utilice [Read](read-method-ado.md) y [Write](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="62c20-p102">The **Type** property determines which methods should be used for reading and writing the **Stream**. For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md). For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>


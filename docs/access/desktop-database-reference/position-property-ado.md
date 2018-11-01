---
title: Position (propiedad, ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab1111cdbc0e5a319f1f3431477854c6d38eff20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875409"
---
# <a name="position-property-ado"></a><span data-ttu-id="a263f-102">Position (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a263f-102">Position property (ADO)</span></span>


<span data-ttu-id="a263f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a263f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a263f-104">Indica la posición actual dentro de un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a263f-104">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a263f-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a263f-105">Settings and return values</span></span>

<span data-ttu-id="a263f-p101">Establece o devuelve un valor de tipo **Long** que especifica el desplazamiento, en número de bytes, de la posición actual desde el principio de la secuencia. El valor predeterminado es 0, que representa el primer byte de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a263f-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="a263f-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a263f-108">Remarks</span></span>

<span data-ttu-id="a263f-p102">La posición actual puede moverse a un punto situado detrás del final de la secuencia. Si se especifica la posición actual detrás del fin de la secuencia, el [tamaño](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) del objeto **Stream** aumentará en consecuencia. Cualquier byte nuevo agregado de esta forma será nulo.</span><span class="sxs-lookup"><span data-stu-id="a263f-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a263f-p103">[!NOTA] <STRONG>Position</STRONG> siempre mide bytes. En las secuencias de texto que usan juegos de caracteres multibyte, multiplique la posición por el tamaño de los caracteres para determinar el número de caracteres. Por ejemplo, en un juego de caracteres de dos bytes, el primer carácter se encuentra en la posición 0, el segundo en la 2, el tercero en la 4 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="a263f-p103"><STRONG>Position</STRONG> always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span></P>



<span data-ttu-id="a263f-p104">No es posible utilizar valores negativos para cambiar la posición actual en un objeto **Stream**. Con **Position** sólo se pueden utilizar números positivos.</span><span class="sxs-lookup"><span data-stu-id="a263f-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="a263f-p105">En los objetos **Stream** de sólo lectura, ADO no devolverá un error si **Position** se establece en un valor superior al **tamaño** de **Stream**. Eso no modifica el tamaño de **Stream** ni altera el contenido de **Stream** de ninguna forma. Sin embargo, debe evitarse, ya que da lugar a un valor de **Position** sin sentido.</span><span class="sxs-lookup"><span data-stu-id="a263f-p105">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>


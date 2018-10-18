---
<span data-ttu-id="6dbd0-101"><<<<<<< Título HEAD: posición (propiedad) (ADO) TOCTitle: posición (propiedad) (ADO) === título: posición (propiedad, ADO) TOCTitle: posición (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6dbd0-101"><<<<<<< HEAD title: Position Property (ADO) TOCTitle: Position Property (ADO) ======= title: Position property (ADO) TOCTitle: Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6dbd0-102">Master ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: ms.date 48546709: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="6dbd0-102">master ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: 48546709 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6dbd0-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6dbd0-103"><<<<<<< HEAD</span></span>
# <a name="position-property-ado"></a><span data-ttu-id="6dbd0-104">Position (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6dbd0-104">Position Property (ADO)</span></span>
=======
# <a name="position-property-ado"></a><span data-ttu-id="6dbd0-105">Posición (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6dbd0-105">Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6dbd0-106">master</span><span class="sxs-lookup"><span data-stu-id="6dbd0-106">master</span></span>


<span data-ttu-id="6dbd0-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dbd0-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6dbd0-108">Indica la posición actual dentro de un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6dbd0-108">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

<span data-ttu-id="6dbd0-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6dbd0-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="6dbd0-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6dbd0-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="6dbd0-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6dbd0-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="6dbd0-112">master</span><span class="sxs-lookup"><span data-stu-id="6dbd0-112">master</span></span>

<span data-ttu-id="6dbd0-p101">Establece o devuelve un valor de tipo **Long** que especifica el desplazamiento, en número de bytes, de la posición actual desde el principio de la secuencia. El valor predeterminado es 0, que representa el primer byte de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6dbd0-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dbd0-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6dbd0-115">Remarks</span></span>

<span data-ttu-id="6dbd0-p102">La posición actual puede moverse a un punto situado detrás del final de la secuencia. Si se especifica la posición actual detrás del fin de la secuencia, el [tamaño](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) del objeto **Stream** aumentará en consecuencia. Cualquier byte nuevo agregado de esta forma será nulo.</span><span class="sxs-lookup"><span data-stu-id="6dbd0-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6dbd0-p103">[!NOTA] <STRONG>Position</STRONG> siempre mide bytes. En las secuencias de texto que usan juegos de caracteres multibyte, multiplique la posición por el tamaño de los caracteres para determinar el número de caracteres. Por ejemplo, en un juego de caracteres de dos bytes, el primer carácter se encuentra en la posición 0, el segundo en la 2, el tercero en la 4 y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="6dbd0-p103"><STRONG>Position</STRONG> always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span></P>



<span data-ttu-id="6dbd0-p104">No es posible utilizar valores negativos para cambiar la posición actual en un objeto **Stream**. Con **Position** sólo se pueden utilizar números positivos.</span><span class="sxs-lookup"><span data-stu-id="6dbd0-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="6dbd0-p105">En los objetos **Stream** de sólo lectura, ADO no devolverá un error si **Position** se establece en un valor superior al **tamaño** de **Stream**. Eso no modifica el tamaño de **Stream** ni altera el contenido de **Stream** de ninguna forma. Sin embargo, debe evitarse, ya que da lugar a un valor de **Position** sin sentido.</span><span class="sxs-lookup"><span data-stu-id="6dbd0-p105">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>


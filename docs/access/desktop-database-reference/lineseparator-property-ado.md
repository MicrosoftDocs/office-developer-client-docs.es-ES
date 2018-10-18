---
<span data-ttu-id="f3bf6-101"><<<<<<< Título HEAD: LineSeparator (propiedad) (ADO) TOCTitle: LineSeparator (propiedad) (ADO) === título: LineSeparator (propiedad, ADO) TOCTitle: LineSeparator (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f3bf6-101"><<<<<<< HEAD title: LineSeparator Property (ADO) TOCTitle: LineSeparator Property (ADO) ======= title: LineSeparator property (ADO) TOCTitle: LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f3bf6-102">Master ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: ms.date 48546676: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="f3bf6-102">master ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: 48546676 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f3bf6-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f3bf6-103"><<<<<<< HEAD</span></span>
# <a name="lineseparator-property-ado"></a><span data-ttu-id="f3bf6-104">LineSeparator (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f3bf6-104">LineSeparator Property (ADO)</span></span>
=======
# <a name="lineseparator-property-ado"></a><span data-ttu-id="f3bf6-105">LineSeparator (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f3bf6-105">LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f3bf6-106">master</span><span class="sxs-lookup"><span data-stu-id="f3bf6-106">master</span></span>


<span data-ttu-id="f3bf6-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3bf6-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f3bf6-108">Indica el carácter binario que se utiliza como separador de línea en objetos de texto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f3bf6-108">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

<span data-ttu-id="f3bf6-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f3bf6-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="f3bf6-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f3bf6-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="f3bf6-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f3bf6-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="f3bf6-112">master</span><span class="sxs-lookup"><span data-stu-id="f3bf6-112">master</span></span>

<span data-ttu-id="f3bf6-p101">Establece o devuelve un valor de tipo [LineSeparatorsEnum](lineseparatorsenum.md) que indica el carácter separador de línea utilizado en el objeto **Stream**. El valor predeterminado es **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3bf6-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3bf6-115">Remarks</span></span>

<span data-ttu-id="f3bf6-p102">**LineSeparator** se utiliza para interpretar líneas al leer el contenido de un objeto de texto **Stream**. Las líneas se pueden omitir con el método [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f3bf6-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="f3bf6-p103">**LineSeparator** sólo se utiliza con objetos de texto **Stream** ([Type](type-property-ado-stream.md) es **adTypeText**). Esta propiedad se pasa por alto si **Type** es **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>


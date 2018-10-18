---
<span data-ttu-id="5ebc5-101"><<<<<<< Título HEAD: DefinedSize (propiedad) (ADO) TOCTitle: DefinedSize (propiedad) (ADO) === título: DefinedSize (propiedad, ADO) TOCTitle: DefinedSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="5ebc5-101"><<<<<<< HEAD title: DefinedSize Property (ADO) TOCTitle: DefinedSize Property (ADO) ======= title: DefinedSize property (ADO) TOCTitle: DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5ebc5-102">Master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: ms.date 48546257: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="5ebc5-102">master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5ebc5-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5ebc5-103"><<<<<<< HEAD</span></span>
# <a name="definedsize-property-ado"></a><span data-ttu-id="5ebc5-104">DefinedSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="5ebc5-104">DefinedSize Property (ADO)</span></span>
=======
# <a name="definedsize-property-ado"></a><span data-ttu-id="5ebc5-105">DefinedSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="5ebc5-105">DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5ebc5-106">master</span><span class="sxs-lookup"><span data-stu-id="5ebc5-106">master</span></span>


<span data-ttu-id="5ebc5-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ebc5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5ebc5-108">Indica la capacidad de datos de un objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5ebc5-108">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="5ebc5-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5ebc5-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="5ebc5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ebc5-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="5ebc5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ebc5-111">Return value</span></span>
>>>>>>> <span data-ttu-id="5ebc5-112">master</span><span class="sxs-lookup"><span data-stu-id="5ebc5-112">master</span></span>

<span data-ttu-id="5ebc5-113">Devuelve un valor de tipo **Long** que refleja el tamaño definido de un campo como un número de bytes.</span><span class="sxs-lookup"><span data-stu-id="5ebc5-113">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ebc5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ebc5-114">Remarks</span></span>

<span data-ttu-id="5ebc5-115">Utilice la propiedad **DefinedSize** para determinar la capacidad de datos de un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="5ebc5-115">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="5ebc5-p101">Las propiedades **DefinedSize** y [ActualSize](actualsize-property-ado.md) son diferentes. Por ejemplo, considere un objeto **Field** con un tipo declarado **adVarChar** y un valor de la propiedad **DefinedSize** de 50 que contenga un carácter único. El valor de la propiedad **ActualSize** que devuelve es la longitud del carácter único en bytes.</span><span class="sxs-lookup"><span data-stu-id="5ebc5-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>


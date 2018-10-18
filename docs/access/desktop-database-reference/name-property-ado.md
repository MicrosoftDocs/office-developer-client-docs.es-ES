---
<span data-ttu-id="40355-101"><<<<<<< Título HEAD: nombre (propiedad) (ADO) TOCTitle: nombre (propiedad) (ADO) === título: nombre (propiedad, ADO) TOCTitle: Name (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="40355-101"><<<<<<< HEAD title: Name Property (ADO) TOCTitle: Name Property (ADO) ======= title: Name property (ADO) TOCTitle: Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="40355-102">Master ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: ms.date 48544683: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="40355-102">master ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: 48544683 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="40355-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="40355-103"><<<<<<< HEAD</span></span>
# <a name="name-property-ado"></a><span data-ttu-id="40355-104">Name (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="40355-104">Name Property (ADO)</span></span>
=======
# <a name="name-property-ado"></a><span data-ttu-id="40355-105">Nombre (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="40355-105">Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="40355-106">master</span><span class="sxs-lookup"><span data-stu-id="40355-106">master</span></span>


<span data-ttu-id="40355-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40355-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40355-108">Indica el nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="40355-108">Indicates the name of an object.</span></span>

<span data-ttu-id="40355-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="40355-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="40355-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="40355-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="40355-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="40355-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="40355-112">master</span><span class="sxs-lookup"><span data-stu-id="40355-112">master</span></span>

<span data-ttu-id="40355-113">Establece o devuelve un valor de tipo **String** que indica el nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="40355-113">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="40355-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40355-114">Remarks</span></span>

<span data-ttu-id="40355-115">Utilice la propiedad **Name** para asignar un nombre a un objeto **Command**, **Property**, **Field** o **Parameter** o para recuperar el nombre de cualquiera de éstos.</span><span class="sxs-lookup"><span data-stu-id="40355-115">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="40355-116">El valor es de lectura y escritura en un objeto **Command** y de sólo lectura en un objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="40355-116">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="40355-p101">En un objeto **Field**, **Name** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Name** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="40355-p101">For a **Field** object, **Name** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="40355-p102">En los objetos **Parameter** que aún no se han anexado a la colección [Parameters](parameters-collection-ado.md), la propiedad **Name** es de lectura y escritura. En los objetos **Parameter** anexados y en el resto de los objetos, la propiedad **Name** es de sólo lectura. En una colección, los nombres no tienen que ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="40355-p102">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write. For appended **Parameter** objects and all other objects, the **Name** property is read-only. Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="40355-122">Es posible recuperar la propiedad **Name** de un objeto mediante un número ordinal, tras lo cual se puede hacer referencia al objeto directamente por su nombre.</span><span class="sxs-lookup"><span data-stu-id="40355-122">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="40355-123">Por ejemplo, si rstMain.Properties (20). Name produce Updatability, sucesivo puede hacer referencia a esta propiedad como produce Updatability, sucesivo puede hacer referencia a esta propiedad como rstMain.Properties("Updatability").</span><span class="sxs-lookup"><span data-stu-id="40355-123">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>


---
<span data-ttu-id="d2764-101"><<<<<<< Título HEAD: tipo (propiedad) (ADO) TOCTitle: tipo de propiedad (ADO) === título: escriba (propiedad, ADO) TOCTitle: escriba (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d2764-101"><<<<<<< HEAD title: Type Property (ADO) TOCTitle: Type Property (ADO) ======= title: Type property (ADO) TOCTitle: Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d2764-102">Master ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: ms.date 48543397: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="d2764-102">master ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: 48543397 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d2764-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d2764-103"><<<<<<< HEAD</span></span>
# <a name="type-property-ado"></a><span data-ttu-id="d2764-104">Type (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d2764-104">Type Property (ADO)</span></span>
=======
# <a name="type-property-ado"></a><span data-ttu-id="d2764-105">Tipo (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d2764-105">Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d2764-106">master</span><span class="sxs-lookup"><span data-stu-id="d2764-106">master</span></span>


<span data-ttu-id="d2764-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2764-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2764-108">Indica el tipo operativo o tipo de datos de un objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) o [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d2764-108">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

<span data-ttu-id="d2764-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d2764-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="d2764-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d2764-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="d2764-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d2764-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="d2764-112">master</span><span class="sxs-lookup"><span data-stu-id="d2764-112">master</span></span>

<span data-ttu-id="d2764-113">Establece o devuelve un valor de tipo [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="d2764-113">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2764-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2764-114">Remarks</span></span>

<span data-ttu-id="d2764-p101">En objetos **Parameter**, la propiedad **Type** es de lectura y escritura. En los nuevos objetos **Field** que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Type** sólo es de lectura y escritura después de que se haya especificado la propiedad [Value](value-property-ado.md) del objeto **Field** y el proveedor de datos haya agregado correctamente el nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="d2764-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="d2764-117">En el resto de los objetos, la propiedad **Type** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2764-117">For all other objects, the **Type** property is read-only.</span></span>


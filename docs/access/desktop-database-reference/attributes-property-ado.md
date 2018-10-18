---
<span data-ttu-id="63586-101"><<<<<<< Título HEAD: atributos (propiedad) (ADO) TOCTitle: atributos (propiedad) (ADO) === título: atributos (propiedad, ADO) TOCTitle: atributos (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="63586-101"><<<<<<< HEAD title: Attributes Property (ADO) TOCTitle: Attributes Property (ADO) ======= title: Attributes property (ADO) TOCTitle: Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="63586-102">Master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: ms.date 48544716: 18/09/2015 mtps_version: Office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="63586-102">master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="63586-103">ado210.chm1231117 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="63586-103">ado210.chm1231117 f1_categories:</span></span>
- <span data-ttu-id="63586-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="63586-104">Office.Version=v15</span></span>
---

<span data-ttu-id="63586-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="63586-105"><<<<<<< HEAD</span></span>
# <a name="attributes-property-ado"></a><span data-ttu-id="63586-106">Attributes (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="63586-106">Attributes Property (ADO)</span></span>
=======
# <a name="attributes-property-ado"></a><span data-ttu-id="63586-107">Attributes (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="63586-107">Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="63586-108">master</span><span class="sxs-lookup"><span data-stu-id="63586-108">master</span></span>


<span data-ttu-id="63586-109">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="63586-109">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="63586-110">Propiedad Attributes</span><span class="sxs-lookup"><span data-stu-id="63586-110">Attributes Property</span></span>

<span data-ttu-id="63586-111">Indica una o varias características de un objeto.</span><span class="sxs-lookup"><span data-stu-id="63586-111">Indicates one or more characteristics of an object.</span></span>

<span data-ttu-id="63586-112"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="63586-112"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="63586-113">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="63586-113">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="63586-114">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="63586-114">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="63586-115">master</span><span class="sxs-lookup"><span data-stu-id="63586-115">master</span></span>

<span data-ttu-id="63586-116">Establece o devuelve un valor de tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="63586-116">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="63586-p101">Para un objeto [Connection](connection-object-ado.md), la propiedad **Attributes** es de lectura y escritura, y su valor puede ser la suma de uno o varios valores de [XactAttributeEnum](xactattributeenum.md). El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="63586-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="63586-p102">Para un objeto [Parameter](parameter-object-ado.md), la propiedad **Attributes** es de lectura y escritura, y su valor puede ser la suma de uno o varios valores de [ParameterAttributesEnum](parameterattributesenum.md). El valor predeterminado es **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="63586-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="63586-p103">Para un objeto [Field](field-object-ado.md), la propiedad **Attributes** puede ser la suma de uno o varios valores de [FieldAttributeEnum](fieldattributeenum.md). Normalmente, es de sólo lectura. Sin embargo, para los objetos **Field** nuevos que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Attributes** es de lectura y escritura sólo después de especificarse la propiedad [Value](value-property-ado.md) del objeto **Field** y de agregar el proveedor correctamente el nuevo objeto **Field** mediante una llamada al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="63586-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="63586-123">Para un objeto [Property](property-object-ado.md), la propiedad **Attributes** es de sólo lectura, y su valor puede ser la suma de uno o varios valores de [PropertyAttributesEnum](propertyattributesenum.md).</span><span class="sxs-lookup"><span data-stu-id="63586-123">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="63586-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63586-124">Remarks</span></span>

<span data-ttu-id="63586-125">Utilice la propiedad **Attributes** para establecer o devolver las características de los objetos **Field**, **Property**, [Connection](field-object-ado.md) o [Parameter](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="63586-125">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="63586-p104">Cuando establece varios atributos, puede sumar las constantes apropiadas. Si establece el valor de la propiedad en una suma que incluye constantes incompatibles, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="63586-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="63586-128">**Uso de servicio de datos remotos** Esta propiedad no está disponible en un objeto de **conexión** de cliente.</span><span class="sxs-lookup"><span data-stu-id="63586-128">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>


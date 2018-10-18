---
<span data-ttu-id="964f4-101"><<<<<<< Título HEAD: tamaño (propiedad) (ADO) TOCTitle: tamaño (propiedad) (ADO) === título: tamaño (propiedad, ADO) TOCTitle: tamaño (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="964f4-101"><<<<<<< HEAD title: Size Property (ADO) TOCTitle: Size Property (ADO) ======= title: Size property (ADO) TOCTitle: Size property (ADO)</span></span>
>>>>>>> <span data-ttu-id="964f4-102">Master ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15) ms:contentKeyID: ms.date 48543753: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="964f4-102">master ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15) ms:contentKeyID: 48543753 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="964f4-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="964f4-103"><<<<<<< HEAD</span></span>
# <a name="size-property-ado"></a><span data-ttu-id="964f4-104">Size (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="964f4-104">Size Property (ADO)</span></span>
=======
# <a name="size-property-ado"></a><span data-ttu-id="964f4-105">Tamaño (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="964f4-105">Size property (ADO)</span></span>
>>>>>>> <span data-ttu-id="964f4-106">master</span><span class="sxs-lookup"><span data-stu-id="964f4-106">master</span></span>


<span data-ttu-id="964f4-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="964f4-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="964f4-108">Indica el tamaño máximo en bytes o caracteres de un objeto [Parameter](parameter-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="964f4-108">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

<span data-ttu-id="964f4-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="964f4-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="964f4-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="964f4-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="964f4-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="964f4-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="964f4-112">master</span><span class="sxs-lookup"><span data-stu-id="964f4-112">master</span></span>

<span data-ttu-id="964f4-113">Establece o devuelve un valor de tipo **Long** que indica el tamaño máximo en bytes o caracteres de un valor de un objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="964f4-113">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="964f4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="964f4-114">Remarks</span></span>

<span data-ttu-id="964f4-115">Utilice la propiedad **Size** para determinar el tamaño máximo de los valores que se van a escribir o a leer en la propiedad [Value](value-property-ado.md) de un objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="964f4-115">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="964f4-116">Si se especifica un tipo de datos de longitud variable para un objeto **Parameter** (por ejemplo, cualquiera de tipo **String**, como **adVarChar**), es necesario establecer la propiedad **Size** del objeto antes de anexarlo a la colección [Parameters](parameters-collection-ado.md); de lo contrario, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="964f4-116">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="964f4-117">Si ya se ha anexado el objeto **Parameter** a la colección **Parameters** de un objeto [Command](command-object-ado.md) y se cambia el tipo de datos por uno de longitud variable, es necesario establecer la propiedad **Size** del objeto **Parameter** antes de ejecutar el objeto **Command**; de lo contrario, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="964f4-117">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="964f4-p101">Si se usa el método [Refresh](refresh-method-ado.md) para obtener información de los parámetros del proveedor y devuelve uno o más objetos **Parameter** de tipo de datos de longitud variable, ADO puede asignar memoria a los parámetros según su tamaño máximo potencial, lo que puede provocar un error durante la ejecución. Para evitar errores, se debe establecer la propiedad **Size** de estos parámetros de forma explícita antes de ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="964f4-p101">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution. To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="964f4-120">La propiedad **Size** es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="964f4-120">The **Size** property is read/write.</span></span>


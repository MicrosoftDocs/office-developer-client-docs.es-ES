---
<span data-ttu-id="6242b-101"><<<<<<< Título HEAD: elemento (propiedad) (ADO) TOCTitle: elemento (propiedad) (ADO) === título: Item (propiedad, ADO) TOCTitle: Item (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6242b-101"><<<<<<< HEAD title: Item Property (ADO) TOCTitle: Item Property (ADO) ======= title: Item property (ADO) TOCTitle: Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6242b-102">Master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: ms.date 48545767: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="6242b-102">master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6242b-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6242b-103"><<<<<<< HEAD</span></span>
# <a name="item-property-ado"></a><span data-ttu-id="6242b-104">Item (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6242b-104">Item Property (ADO)</span></span>
=======
# <a name="item-property-ado"></a><span data-ttu-id="6242b-105">Elemento (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6242b-105">Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6242b-106">master</span><span class="sxs-lookup"><span data-stu-id="6242b-106">master</span></span>

<span data-ttu-id="6242b-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6242b-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6242b-108">Indica un miembro específico de una colección, por nombre o número ordinal.</span><span class="sxs-lookup"><span data-stu-id="6242b-108">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6242b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6242b-109">Syntax</span></span>

<span data-ttu-id="6242b-110">*Objeto*de conjunto de = *colección*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="6242b-110">Set*object* = *collection*.Item ( Index )</span></span>

<span data-ttu-id="6242b-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6242b-111"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="6242b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6242b-112">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="6242b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6242b-113">Return value</span></span>
>>>>>>> <span data-ttu-id="6242b-114">master</span><span class="sxs-lookup"><span data-stu-id="6242b-114">master</span></span>

<span data-ttu-id="6242b-115">Devuelve una referencia de objeto.</span><span class="sxs-lookup"><span data-stu-id="6242b-115">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="6242b-116">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6242b-116">Parameters</span></span>

- <span data-ttu-id="6242b-117">*Index*</span><span class="sxs-lookup"><span data-stu-id="6242b-117">*Index*</span></span>

- <span data-ttu-id="6242b-118">Una expresión de tipo **Variant** que evalúa el nombre o el número ordinal de un objeto de una colección.</span><span class="sxs-lookup"><span data-stu-id="6242b-118">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6242b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6242b-119">Remarks</span></span>

<span data-ttu-id="6242b-120">Utilice la propiedad **Item** para devolver un objeto específico de una colección.</span><span class="sxs-lookup"><span data-stu-id="6242b-120">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="6242b-121">Si el **elemento** no se puede encontrar un objeto en la colección que corresponde al argumento *Index* , se produce un error.</span><span class="sxs-lookup"><span data-stu-id="6242b-121">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="6242b-122">Además, algunas colecciones no admiten objetos con nombre; en estas colecciones es necesario utilizar referencias de número ordinal.</span><span class="sxs-lookup"><span data-stu-id="6242b-122">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="6242b-123">**Item** es la propiedad predeterminada para todas las colecciones; por lo tanto, los siguientes formatos de sintaxis son intercambiables:</span><span class="sxs-lookup"><span data-stu-id="6242b-123">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```

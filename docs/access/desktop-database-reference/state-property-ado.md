---
<span data-ttu-id="155df-101"><<<<<<< Título HEAD: estado (propiedad) (ADO) TOCTitle: estado (propiedad) (ADO) === título: estado (propiedad, ADO) TOCTitle: estado (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="155df-101"><<<<<<< HEAD title: State Property (ADO) TOCTitle: State Property (ADO) ======= title: State property (ADO) TOCTitle: State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="155df-102">Master ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: ms.date 48547053: 18/09/2015 mtps_version: Office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="155df-102">master ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="155df-103">ado210.chm1231176 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="155df-103">ado210.chm1231176 f1_categories:</span></span>
- <span data-ttu-id="155df-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="155df-104">Office.Version=v15</span></span>
---

<span data-ttu-id="155df-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="155df-105"><<<<<<< HEAD</span></span>
# <a name="state-property-ado"></a><span data-ttu-id="155df-106">State (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="155df-106">State Property (ADO)</span></span>
=======
# <a name="state-property-ado"></a><span data-ttu-id="155df-107">State (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="155df-107">State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="155df-108">master</span><span class="sxs-lookup"><span data-stu-id="155df-108">master</span></span>


<span data-ttu-id="155df-109">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="155df-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="155df-110">En todos los objetos aplicables indica si el estado del objeto es abierto o cerrado.</span><span class="sxs-lookup"><span data-stu-id="155df-110">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="155df-111">Indica para todos los objetos aplicables que ejecutan un método asincrónico si el objeto se encuentra actualmente en estado de conexión, ejecución o recuperación.</span><span class="sxs-lookup"><span data-stu-id="155df-111">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

<span data-ttu-id="155df-112"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="155df-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="155df-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="155df-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="155df-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="155df-114">Return value</span></span>
>>>>>>> <span data-ttu-id="155df-115">master</span><span class="sxs-lookup"><span data-stu-id="155df-115">master</span></span>

<span data-ttu-id="155df-p101">Devuelve un valor de tipo **Long** que puede ser un valor [ObjectStateEnum](objectstateenum.md). El valor predeterminado es **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="155df-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="155df-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="155df-118">Remarks</span></span>

<span data-ttu-id="155df-119">Puede utilizar la propiedad **Estado (State)** para determinar el estado actual de un objeto dado en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="155df-119">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="155df-p102">La propiedad **Estado (State)** del objeto puede tener una combinación de valores. Por ejemplo, si se está ejecutando una instrucción, esta propiedad tendrá un valor combinado de **adStateOpen** y **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="155df-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="155df-122">La propiedad **Estado (State)** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="155df-122">The **State** property is read-only.</span></span>


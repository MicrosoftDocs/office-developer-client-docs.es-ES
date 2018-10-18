---
<span data-ttu-id="8d1b0-101"><<<<<<< Título HEAD: descripción (propiedad) (ADO) TOCTitle: descripción (propiedad) (ADO) === título: descripción (propiedad, ADO) TOCTitle: descripción (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="8d1b0-101"><<<<<<< HEAD title: Description Property (ADO) TOCTitle: Description Property (ADO) ======= title: Description property (ADO) TOCTitle: Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8d1b0-102">Master ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: ms.date 48544064: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="8d1b0-102">master ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8d1b0-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="8d1b0-103"><<<<<<< HEAD</span></span>
# <a name="description-property-ado"></a><span data-ttu-id="8d1b0-104">Description (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="8d1b0-104">Description Property (ADO)</span></span>
=======
# <a name="description-property-ado"></a><span data-ttu-id="8d1b0-105">Descripción (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="8d1b0-105">Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8d1b0-106">master</span><span class="sxs-lookup"><span data-stu-id="8d1b0-106">master</span></span>


<span data-ttu-id="8d1b0-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d1b0-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d1b0-108">Describe un objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8d1b0-108">Describes an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="8d1b0-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="8d1b0-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="8d1b0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d1b0-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="8d1b0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d1b0-111">Return value</span></span>
>>>>>>> <span data-ttu-id="8d1b0-112">master</span><span class="sxs-lookup"><span data-stu-id="8d1b0-112">master</span></span>

<span data-ttu-id="8d1b0-113">Devuelve un valor de tipo **String** que contiene una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="8d1b0-113">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d1b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d1b0-114">Remarks</span></span>

<span data-ttu-id="8d1b0-p101">Use la propiedad **Description** para obtener una breve descripción del error. Muestre esta propiedad para alertar al usuario sobre un error que no puede o no desea controlar. La cadena procederá de ADO o de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="8d1b0-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="8d1b0-p102">Los proveedores son responsables de especificar el texto del error específico a ADO. ADO agrega un objeto [Error](error-object-ado.md) a la colección **Errors** por cada error o advertencia que recibe del proveedor. Enumere la colección **Errors** para rastrear los errores que especifica el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8d1b0-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>


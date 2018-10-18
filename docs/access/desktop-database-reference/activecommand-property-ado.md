---
<span data-ttu-id="17dd0-101"><<<<<<< Título HEAD: ActiveCommand (propiedad) (ADO) TOCTitle: ms:assetid de la propiedad ActiveCommand (ADO): 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: ms.date 48544459: 18/09/2015 mtps_version: v = Office.15</span><span class="sxs-lookup"><span data-stu-id="17dd0-101"><<<<<<< HEAD title: ActiveCommand Property (ADO) TOCTitle: ActiveCommand Property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="17dd0-102">ActiveCommand (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="17dd0-102">ActiveCommand Property (ADO)</span></span>

<span data-ttu-id="17dd0-103">=== título: ActiveCommand (propiedad, ADO) TOCTitle: ActiveCommand (propiedad, ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: ms.date 48544459: 17/10/2018 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="17dd0-103">======= title: ActiveCommand property (ADO) TOCTitle: ActiveCommand property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="17dd0-104">ActiveCommand (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="17dd0-104">ActiveCommand property (ADO)</span></span>
>>>>>>> <span data-ttu-id="17dd0-105">master</span><span class="sxs-lookup"><span data-stu-id="17dd0-105">master</span></span>

<span data-ttu-id="17dd0-106">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17dd0-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17dd0-107">Indica el objeto [Command](command-object-ado.md) que ha creado el objeto [Recordset](recordset-object-ado.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="17dd0-107">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="17dd0-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="17dd0-108"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="17dd0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17dd0-109">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="17dd0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17dd0-110">Return value</span></span>
>>>>>>> <span data-ttu-id="17dd0-111">master</span><span class="sxs-lookup"><span data-stu-id="17dd0-111">master</span></span>

<span data-ttu-id="17dd0-p101">Devuelve un valor de tipo **Variant** que contiene un objeto **Command**. El valor predeterminado es una referencia de objeto nula.</span><span class="sxs-lookup"><span data-stu-id="17dd0-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="17dd0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17dd0-114">Remarks</span></span>

<span data-ttu-id="17dd0-115">La propiedad **ActiveCommand** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="17dd0-115">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="17dd0-116"><<<<<<< HEAD si un objeto **Command** no se usó para crear el **objeto Recordset**actual, a continuación, se devuelve una referencia de objeto **Null** .</span><span class="sxs-lookup"><span data-stu-id="17dd0-116"><<<<<<< HEAD If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>
<span data-ttu-id="17dd0-117">=== Si un objeto **Command** no se usó para crear el **objeto Recordset**actual, se devuelve una referencia de objeto **Null** .</span><span class="sxs-lookup"><span data-stu-id="17dd0-117">======= If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>
>>>>>>> <span data-ttu-id="17dd0-118">master</span><span class="sxs-lookup"><span data-stu-id="17dd0-118">master</span></span>

<span data-ttu-id="17dd0-119">Use esta propiedad para buscar el objeto **Command** asociado cuando solo dispone del objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="17dd0-119">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>


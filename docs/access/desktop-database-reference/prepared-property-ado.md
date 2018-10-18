---
<span data-ttu-id="dfff4-101"><<<<<<< Título HEAD: preparado (propiedad) (ADO) TOCTitle: preparado (propiedad) (ADO) === título: preparado (propiedad, ADO) TOCTitle: preparado (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="dfff4-101"><<<<<<< HEAD title: Prepared Property (ADO) TOCTitle: Prepared Property (ADO) ======= title: Prepared property (ADO) TOCTitle: Prepared property (ADO)</span></span>
>>>>>>> <span data-ttu-id="dfff4-102">Master ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID: ms.date 48544116: 18/09/2015 mtps_version: Office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="dfff4-102">master ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID: 48544116 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="dfff4-103">ado210.chm1231161 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="dfff4-103">ado210.chm1231161 f1_categories:</span></span>
- <span data-ttu-id="dfff4-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="dfff4-104">Office.Version=v15</span></span>
---

<span data-ttu-id="dfff4-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="dfff4-105"><<<<<<< HEAD</span></span>
# <a name="prepared-property-ado"></a><span data-ttu-id="dfff4-106">Prepared (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="dfff4-106">Prepared Property (ADO)</span></span>
=======
# <a name="prepared-property-ado"></a><span data-ttu-id="dfff4-107">Prepared (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="dfff4-107">Prepared property (ADO)</span></span>
>>>>>>> <span data-ttu-id="dfff4-108">master</span><span class="sxs-lookup"><span data-stu-id="dfff4-108">master</span></span>


<span data-ttu-id="dfff4-109">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfff4-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dfff4-110">Indica si se va a guardar una versión compilada de un comando antes de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="dfff4-110">Indicates whether to save a compiled version of a command before execution.</span></span>

<span data-ttu-id="dfff4-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="dfff4-111"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="dfff4-112">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="dfff4-112">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="dfff4-113">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="dfff4-113">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="dfff4-114">master</span><span class="sxs-lookup"><span data-stu-id="dfff4-114">master</span></span>

<span data-ttu-id="dfff4-115">Establece o devuelve un valor de tipo **Boolean** que, si se establece en **True**, indica que debe prepararse el comando.</span><span class="sxs-lookup"><span data-stu-id="dfff4-115">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfff4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfff4-116">Remarks</span></span>

<span data-ttu-id="dfff4-p101">Use la propiedad **Prepared** para que el proveedor guarde una versión preparada (o compilada) de la consulta especificada en la propiedad [CommandText](commandtext-property-ado.md) antes de la primera ejecución de un objeto [Command](command-object-ado.md). Esto puede ralentizar la primera ejecución de un comando, pero una vez que el proveedor lo compila, usará la versión compilada del comando para todas las ejecuciones siguientes, lo que dará lugar a una mejora del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="dfff4-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="dfff4-119">Si la propiedad es **False**, el proveedor ejecutará el objeto **Command** directamente sin crear una versión compilada.</span><span class="sxs-lookup"><span data-stu-id="dfff4-119">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="dfff4-p102">Si el proveedor no admite la preparación del comando, puede devolver un error en cuanto esta propiedad se establezca en **True**. Si no devuelve un error, simplemente omite la solicitud de preparar el comando y establece la propiedad **Prepared** en **False**.</span><span class="sxs-lookup"><span data-stu-id="dfff4-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>


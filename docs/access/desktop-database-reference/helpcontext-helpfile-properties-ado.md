---
<span data-ttu-id="ec018-101"><<<<<<< Título HEAD: ContextoDeAyuda (HelpContext), las propiedades HelpFile (ADO) TOCTitle: ContextoDeAyuda (HelpContext), las propiedades HelpFile (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 18/09 / 2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="ec018-101"><<<<<<< HEAD title: HelpContext, HelpFile Properties (ADO) TOCTitle: HelpContext, HelpFile Properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="ec018-102">Propiedades ContextoDeAyuda (HelpContext), HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec018-102">HelpContext, HelpFile Properties (ADO)</span></span>

<span data-ttu-id="ec018-103">=== título: ContextoDeAyuda (HelpContext), HelpFile propiedades (ADO) TOCTitle: ContextoDeAyuda (HelpContext), HelpFile (ADO) propiedades ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 17/10/2018 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="ec018-103">======= title: HelpContext, HelpFile properties (ADO) TOCTitle: HelpContext, HelpFile properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="ec018-104">ContextoDeAyuda (HelpContext), HelpFile propiedades (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec018-104">HelpContext, HelpFile properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="ec018-105">master</span><span class="sxs-lookup"><span data-stu-id="ec018-105">master</span></span>

<span data-ttu-id="ec018-106">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec018-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ec018-107">Indican el archivo de Ayuda y el tema asociados a un objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ec018-107">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="ec018-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ec018-108"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="ec018-109">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ec018-109">Return Values</span></span>

  - <span data-ttu-id="ec018-110">**HelpContextID**: devuelve un identificador de contexto, como un valor de tipo **Long**, de un tema de un archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="ec018-110">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="ec018-111">**HelpFile**: devuelve un valor de tipo **String** que evalúa una ruta de acceso completa resuelta a un archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="ec018-111">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="ec018-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ec018-112">Return values</span></span>

- <span data-ttu-id="ec018-113">**HelpContextID**: devuelve un identificador de contexto, como un valor de tipo **Long**, de un tema de un archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="ec018-113">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="ec018-114">**HelpFile**: devuelve un valor de tipo **String** que evalúa una ruta de acceso completa resuelta a un archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="ec018-114">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
>>>>>>> <span data-ttu-id="ec018-115">master</span><span class="sxs-lookup"><span data-stu-id="ec018-115">master</span></span>

## <a name="remarks"></a><span data-ttu-id="ec018-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec018-116">Remarks</span></span>

<span data-ttu-id="ec018-p101">Si se especifica un archivo de Ayuda en la propiedad **HelpFile**, la propiedad **ContextoDeAyuda (HelpContext)** se utiliza para mostrar automáticamente el tema de Ayuda que identifica. Si no hay ningún tema de Ayuda pertinente disponible, la propiedad **ContextoDeAyuda (HelpContext)** devuelve cero y la propiedad **HelpFile** devuelve una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="ec018-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>


---
title: ActiveConnection (propiedad, ADO)
TOCTitle: ActiveConnection Property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d44a17d192abdb68755a2010184b4fb4d6531174
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486757"
---
# <a name="activeconnection-property-ado"></a><span data-ttu-id="92652-102">ActiveConnection (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="92652-102">ActiveConnection Property (ADO)</span></span>


<span data-ttu-id="92652-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="92652-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92652-104">Indica a qué objeto [Connection](connection-object-ado.md) pertenece actualmente el objeto [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) o [Record](record-object-ado.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="92652-104">Indicates to which [Connection](connection-object-ado.md) object the specified [Command](command-object-ado.md), [Recordset](recordset-object-ado.md), or [Record](record-object-ado.md) object currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="92652-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="92652-105">Settings and Return Values</span></span>

<span data-ttu-id="92652-p101">Establece o devuelve un valor de tipo **String** que contiene la definición de una conexión si la conexión está cerrada, o bien, **Variant** que contiene el actual objeto **Connection** si la conexión está abierta. El valor predeterminado es una referencia de objeto nula. Vea la propiedad [ConnectionString](connectionstring-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="92652-p101">Sets or returns a **String** value that contains a definition for a connection if the connection is closed, or a **Variant** containing the current **Connection** object if the connection is open. Default is a null object reference. See the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="92652-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92652-109">Remarks</span></span>

<span data-ttu-id="92652-110">Use la propiedad **ActiveConnection** para determinar el objeto **Connection** a través del cual se va a ejecutar el objeto **Command** especificado o se va a abrir el objeto **Recordset** especificado.</span><span class="sxs-lookup"><span data-stu-id="92652-110">Use the **ActiveConnection** property to determine the **Connection** object over which the specified **Command** object will execute or the specified **Recordset** will be opened.</span></span>

<span data-ttu-id="92652-111">**Command**</span><span class="sxs-lookup"><span data-stu-id="92652-111">**Command**</span></span>

<span data-ttu-id="92652-112">Para los objetos **Command**, la propiedad **ActiveConnection** es de lectura y de escritura.</span><span class="sxs-lookup"><span data-stu-id="92652-112">For **Command** objects, the **ActiveConnection** property is read/write.</span></span>

<span data-ttu-id="92652-113">Si se intenta llamar al método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) en un objeto **Command** antes de que se establezca esta propiedad en un objeto **Connection** abierto o una cadena de conexión válida, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="92652-113">If you attempt to call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method on a **Command** object before setting this property to an open **Connection** object or valid connection string, an error occurs.</span></span>

<span data-ttu-id="92652-114">**Microsoft Visual Basic** Establecer la propiedad **ActiveConnection** en *Nothing* desasocia el objeto **Command** de la actual **conexión** y hace que el proveedor liberar todos los recursos asociados en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="92652-114">**Microsoft Visual Basic**Setting the **ActiveConnection** property to *Nothing* disassociates the **Command** object from the current **Connection** and causes the provider to release any associated resources on the data source.</span></span> <span data-ttu-id="92652-115">A continuación, se puede asociar el objeto **Command** al mismo objeto **Connection** o a otro.</span><span class="sxs-lookup"><span data-stu-id="92652-115">You can then associate the **Command** object with the same or another **Connection** object.</span></span> <span data-ttu-id="92652-116">Algunos proveedores permiten cambiar el valor de la propiedad de una **conexión** a otro, sin tener que establecer primero la propiedad en *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="92652-116">Some providers allow you to change the property setting from one **Connection** to another, without having to first set the property to *Nothing*.</span></span>

<span data-ttu-id="92652-117">Si la colección [Parameters](parameters-collection-ado.md) del objeto **Command** contiene parámetros proporcionados por el proveedor, se borra la colección si se establece la propiedad **ActiveConnection** en *Nothing* o en otro objeto de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="92652-117">If the [Parameters](parameters-collection-ado.md) collection of the **Command** object contains parameters supplied by the provider, the collection is cleared if you set the **ActiveConnection** property to *Nothing* or to another **Connection** object.</span></span> <span data-ttu-id="92652-118">Si manualmente crear objetos [Parameter](parameter-object-ado.md) y usarlos para rellenar la colección **Parameters** del objeto **Command** , establecer **ActiveConnection** deja propiedad en *Nothing* o en otro objeto de **conexión** la colección **Parameters** intacta.</span><span class="sxs-lookup"><span data-stu-id="92652-118">If you manually create [Parameter](parameter-object-ado.md) objects and use them to fill the **Parameters** collection of the **Command** object, setting the **ActiveConnection** property to *Nothing* or to another **Connection** object leaves the **Parameters** collection intact.</span></span>

<span data-ttu-id="92652-p104">Al cerrar el objeto **Connection** al que está asociado un objeto *Command*, el valor de la propiedad **ActiveConnection** se establece en **Nothing**. Si se establece esta propiedad en un objeto **Connection** cerrado, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="92652-p104">Closing the **Connection** object with which a **Command** object is associated sets the **ActiveConnection** property to *Nothing*. Setting this property to a closed **Connection** object generates an error.</span></span>

<span data-ttu-id="92652-121">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="92652-121">**Recordset**</span></span>

<span data-ttu-id="92652-p105">Para los objetos **Recordset** abiertos u objetos **Recordset** cuya propiedad [Source](source-property-ado-recordset.md) está establecida en un objeto **Command** válido, la propiedad **ActiveConnection** es de sólo lectura. En caso contrario, es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="92652-p105">For open **Recordset** objects or for **Recordset** objects whose [Source](source-property-ado-recordset.md) property is set to a valid **Command** object, the **ActiveConnection** property is read-only. Otherwise, it is read/write.</span></span>

<span data-ttu-id="92652-p106">Esta propiedad se puede establecer en un objeto **Connection** válido o en una cadena de conexión válida. En este caso, el proveedor crea un nuevo objeto **Connection** mediante esta definición y abre la conexión. Además, el proveedor puede establecer esta propiedad en el nuevo objeto **Connection** para permitir al usuario obtener acceso al objeto **Connection** con el fin de obtener amplia información de errores o ejecutar otros comandos.</span><span class="sxs-lookup"><span data-stu-id="92652-p106">You can set this property to a valid **Connection** object or to a valid connection string. In this case, the provider creates a new **Connection** object using this definition and opens the connection. Additionally, the provider may set this property to the new **Connection** object to give you a way to access the **Connection** object for extended error information or to execute other commands.</span></span>

<span data-ttu-id="92652-127">Si utiliza el argumento *ActiveConnection* del método [Open](open-method-ado-recordset.md) para abrir un objeto **Recordset** , la propiedad **ActiveConnection** heredará el valor del argumento.</span><span class="sxs-lookup"><span data-stu-id="92652-127">If you use the *ActiveConnection* argument of the [Open](open-method-ado-recordset.md) method to open a **Recordset** object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="92652-128">Si se establece la propiedad **Source** del objeto **Recordset** en una variable del objeto **Command**, la propiedad **ActiveConnection** del objeto **Recordset** hereda el valor de la propiedad **ActiveConnection** del objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="92652-128">If you set the **Source** property of the **Recordset** object to a valid **Command** object variable, the **ActiveConnection** property of the **Recordset** inherits the setting of the **Command** object's **ActiveConnection** property.</span></span>

<span data-ttu-id="92652-129">**Uso de servicio de datos remotos** Cuando se usa en un objeto Recordset de cliente, esta propiedad puede establecerse sólo en una cadena de conexión o (en Microsoft Visual Basic o Visual Basic Scripting Edition) en *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="92652-129">**Remote Data Service Usage**When used on a client-side Recordset object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to *Nothing*.</span></span>

<span data-ttu-id="92652-130">**Record**</span><span class="sxs-lookup"><span data-stu-id="92652-130">**Record**</span></span>

<span data-ttu-id="92652-p107">Esta propiedad es de lectura y escritura cuando el objeto **Record** está cerrado, y puede contener una cadena de conexión o una referencia a un objeto **Connection** abierto. Esta propiedad es de sólo lectura cuando el objeto **Record** está abierto, y contiene una referencia a un objeto **Connection** abierto.</span><span class="sxs-lookup"><span data-stu-id="92652-p107">This property is read/write when the **Record** object is closed, and may contain a connection string or reference to an open **Connection** object. This property is read-only when the **Record** object is open, and contains a reference to an open **Connection** object.</span></span>

<span data-ttu-id="92652-p108">Se crea implícitamente un objeto **Connection** cuando se abre el objeto **Record** desde una dirección URL. Abra el objeto **Record** con un objeto **Connection** existente abierto asignando el objeto **Connection** a esta propiedad o utilizando el objeto **Connection** como parámetro en la llamada al método [Open](open-method-ado-record.md). Si se abre el objeto **Record** desde un objeto **Record** o [Recordset](recordset-object-ado.md) existente, se asocia automáticamente al objeto **Connection** de ese objeto **Record** o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="92652-p108">A **Connection** object is created implicitly when the **Record** object is opened from a URL. Open the **Record** with an existing, open **Connection** object by assigning the **Connection** object to this property, or using the **Connection** object as a parameter in the [Open](open-method-ado-record.md) method call. If the **Record** is opened from an existing **Record** or [Recordset](recordset-object-ado.md), then it is automatically associated with that **Record** or **Recordset** object's **Connection** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="92652-p109">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="92652-p109">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>



---
title: Guardar método - ActiveX Data Objects (ADO)
TOCTitle: Save Method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd77102d178399afeb3ebcb493799e83467c4687
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486627"
---
# <a name="save-method-ado"></a><span data-ttu-id="ec891-102">Save (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="ec891-102">Save Method (ADO)</span></span>


<span data-ttu-id="ec891-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec891-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ec891-104">Guarda el objeto [Recordset](recordset-object-ado.md) en un archivo o un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ec891-104">Saves the [Recordset](recordset-object-ado.md) in a file or [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec891-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec891-105">Syntax</span></span>

<span data-ttu-id="ec891-106">*conjunto de registros*. Guardar*destino*, *PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="ec891-106">*recordset*.Save*Destination*, *PersistFormat*</span></span>

## <a name="parameters"></a><span data-ttu-id="ec891-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec891-107">Parameters</span></span>

  - <span data-ttu-id="ec891-108">*Destination*</span><span class="sxs-lookup"><span data-stu-id="ec891-108">*Destination*</span></span>

  - <span data-ttu-id="ec891-p101">Es opcional. **Variant** que representa la ruta de acceso completa al archivo donde se va a guardar el objeto **Recordset** o una referencia a un objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="ec891-p101">Optional. A **Variant** that represents the complete path name of the file where the **Recordset** is to be saved, or a reference to a **Stream** object.</span></span>

  - <span data-ttu-id="ec891-111">*PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="ec891-111">*PersistFormat*</span></span>

  - <span data-ttu-id="ec891-p102">Es opcional. Valor de [PersistFormatEnum](persistformatenum.md) que especifica el formato en el que se va a guardar el objeto **Recordset** (XML o ADTG). El valor predeterminado es **adPersistADTG**.</span><span class="sxs-lookup"><span data-stu-id="ec891-p102">Optional. A [PersistFormatEnum](persistformatenum.md) value that specifies the format in which the **Recordset** is to be saved (XML or ADTG). The default value is **adPersistADTG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec891-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec891-115">Remarks</span></span>

<span data-ttu-id="ec891-p103">El método **Save** se puede invocar únicamente en un objeto **Recordset** abierto. Utilice el método [Open](open-method-ado-recordset.md) para restaurar posteriormente el objeto **Recordset** desde *Destination*.</span><span class="sxs-lookup"><span data-stu-id="ec891-p103">The **Save** method can only be invoked on an open **Recordset**. Use the [Open](open-method-ado-recordset.md) method to later restore the **Recordset** from *Destination*.</span></span>

<span data-ttu-id="ec891-p104">Si se estableció la propiedad [Filter](filter-property-ado.md) para el objeto **Recordset**, se guardan únicamente las filas accesibles con el filtro activado. Si el objeto **Recordset** es jerárquico, se guardan el **Recordset** secundario actual y sus elementos secundarios, incluido el objeto **Recordset** primario. Si se invoca el método **Save** de un objeto **Recordset** secundario, se guardan el objeto secundario y todos sus elementos secundarios, pero no se guarda el objeto primario.</span><span class="sxs-lookup"><span data-stu-id="ec891-p104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span>

<span data-ttu-id="ec891-p105">La primera vez que se guarda el **conjunto de registros**, la especificación de *Destination* es opcional. Si se omite *Destination*, se creará un nuevo archivo con un nombre establecido en el valor de la propiedad [Origen](source-property-ado-recordset.md) del **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="ec891-p105">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="ec891-123">Se omite *Destination* cuando se vuelve a llamar a **Guardar** después de la primera o se producirá un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ec891-123">Omit *Destination* when you subsequently call **Save** after the first save, or a run-time error will occur.</span></span> <span data-ttu-id="ec891-124">Si se llama posteriormente **Guardar** con un nuevo *destino*, se guarda el **objeto Recordset** en el nuevo destino.</span><span class="sxs-lookup"><span data-stu-id="ec891-124">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="ec891-125">Sin embargo, tanto el nuevo destino como el original estarán abiertos.</span><span class="sxs-lookup"><span data-stu-id="ec891-125">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="ec891-p107">El método **Save** no cierra el objeto **Recordset** ni el valor especificado por *Destination*, por lo que se puede seguir trabajando con el objeto **Recordset** y se pueden guardar los cambios más recientes. *Destination* permanecerá abierto hasta que se cierre el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ec891-p107">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed.</span></span>

<span data-ttu-id="ec891-p108">Por motivos de seguridad, el método **Save** sólo permite el uso de configuraciones de seguridad baja y personalizada desde un script ejecutado por Microsoft Internet Explorer. Para obtener una explicación más detallada de los problemas de seguridad, vea el tema sobre los problemas de seguridad de ADO y RDS en Microsoft Internet Explorer, que se encuentra en los artículos técnicos de ActiveX Data Objects (ADO), en la sección de artículos técnicos de Microsoft Data Access.</span><span class="sxs-lookup"><span data-stu-id="ec891-p108">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="ec891-130">Si se llama al método **Save** mientras hay en curso una operación asincrónica de recuperación, ejecución o actualización de un objeto **Recordset**, **Save** esperará hasta que finalice la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ec891-130">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, then **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="ec891-p109">Los registros se guardan comenzando por la primera fila del objeto **Recordset**. Cuando finalice el método **Save**, la posición de fila actual se moverá hasta la primera fila del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ec891-p109">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="ec891-p110">Para obtener los mejores resultados, establezca el valor de la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient** con el método **Save**. Si el proveedor no admite todas las funciones necesarias para guardar los objetos **Recordset**, el Servicio de cursores las proporcionará.</span><span class="sxs-lookup"><span data-stu-id="ec891-p110">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="ec891-p111">Cuando se almacena un objeto **Recordset** con el valor de la propiedad **CursorLocation** establecido en **adUseServer**, la función de actualización del objeto **Recordset** es limitada. Normalmente, solo se permiten eliminaciones, inserciones y actualizaciones de una sola tabla (según la funcionalidad del proveedor). El método [Resync](resync-method-ado.md) tampoco está disponible en esta configuración.</span><span class="sxs-lookup"><span data-stu-id="ec891-p111">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ec891-138">[!NOTA] El almacenamiento de un objeto <STRONG>Recordset</STRONG> con <STRONG>campos</STRONG> de tipo <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG> o <STRONG>adIUnknown</STRONG> no lo admite ADO y puede generar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="ec891-138">Saving a <STRONG>Recordset</STRONG> with <STRONG>Fields</STRONG> of type <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG>, or <STRONG>adIUnknown</STRONG> is not supported by ADO and can cause unpredictable results.</span></span></P>



<span data-ttu-id="ec891-139">Sólo los **filtros** con el formato de las cadenas de criterios (por ejemplo, FechaPedido \> ' 12/31/1999 ') afectan al contenido de un **objeto Recordset**de persistentes.</span><span class="sxs-lookup"><span data-stu-id="ec891-139">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="ec891-140">Los filtros creados con una matriz de **marcadores** o mediante un valor de **FilterGroupEnum** no afectan al contenido del objeto **Recordset** almacenado.</span><span class="sxs-lookup"><span data-stu-id="ec891-140">Filters created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted **Recordset**.</span></span> <span data-ttu-id="ec891-141">Estas reglas se aplican a los objetos **Recordset** creados con cursores de cliente o de servidor.</span><span class="sxs-lookup"><span data-stu-id="ec891-141">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

<span data-ttu-id="ec891-142">Debido a que el parámetro *Destination* puede aceptar cualquier objeto que admita la interfaz IStream de OLE DB, puede guardar un **objeto Recordset** directamente en el objeto Response de ASP.</span><span class="sxs-lookup"><span data-stu-id="ec891-142">Because the *Destination* parameter can accept any object that supports the OLE DB IStream interface, you can save a **Recordset** directly to the ASP Response object.</span></span> <span data-ttu-id="ec891-143">Para obtener más información, vea [Escenario de almacenamiento de un objeto Recordset en formato XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="ec891-143">For more details, please see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

<span data-ttu-id="ec891-144">También se puede guardar un objeto **Recordset** con formato XML en una instancia de un objeto DOM MSXML, tal y como se muestra en el código siguiente de Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ec891-144">You can also save a **Recordset** in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</span></span>


> [!NOTE]
> <P><span data-ttu-id="ec891-p114">[!NOTA] Existen dos limitaciones cuando se guardan objetos <STRONG>Recordset</STRONG> jerárquicos (formas de datos) en formato XML: no se puede guardar en XML si el objeto <STRONG>Recordset</STRONG> jerárquico contiene actualizaciones pendientes y no se puede guardar un objeto <STRONG>Recordset</STRONG> jerárquico parametrizado.</span><span class="sxs-lookup"><span data-stu-id="ec891-p114">Two limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. You cannot save into XML if the hierarchical <STRONG>Recordset</STRONG> contains pending updates, and you cannot save a parameterized hierarchical <STRONG>Recordset</STRONG>.</span></span></P>



<span data-ttu-id="ec891-p115">Un objeto Recordset guardado en formato XML se guarda mediante el formato UTF-8. Cuando ese archivo se carga en un objeto Stream de ADO, este objeto no intentará abrir un objeto Recordset de la secuencia, a menos que la propiedad Charset de la secuencia tenga el valor apropiado para el formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="ec891-p115">A Recordset saved in XML format is saved using UTF-8 format. When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</span></span>

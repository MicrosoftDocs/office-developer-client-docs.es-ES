---
title: Value (propiedad, ADO)
TOCTitle: Value Property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68c0d45345dfc768f5d435689abf67bcc3d9abe2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483567"
---
# <a name="value-property-ado"></a><span data-ttu-id="d8fd1-102">Value (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d8fd1-102">Value Property (ADO)</span></span>


<span data-ttu-id="d8fd1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8fd1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d8fd1-104">Indica el valor asignado a un objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) o [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d8fd1-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d8fd1-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d8fd1-105">Settings and Return Values</span></span>

<span data-ttu-id="d8fd1-p101">Establece o devuelve un valor de tipo **Variant** que indica el valor del objeto. El valor predeterminado depende de la propiedad [Type](type-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d8fd1-p101">Sets or returns a **Variant** value that indicates the value of the object. Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fd1-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8fd1-108">Remarks</span></span>

<span data-ttu-id="d8fd1-p102">Utilice la propiedad **Value** para establecer o devolver datos de objetos **Field**, para establecer o devolver valores de parámetros con objetos **Parameter** o para establecer o devolver la configuración de las propiedades con objetos **Property**. El que la propiedad **Value** sea de lectura o escritura o de sólo lectura depende de varios factores; vea el tema correspondiente a cada objeto para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d8fd1-p102">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects. Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="d8fd1-111">ADO permite establecer y devolver datos binarios largos con la propiedad **Value**.</span><span class="sxs-lookup"><span data-stu-id="d8fd1-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d8fd1-p103">[!NOTA] En los objetos <STRONG>Parameter</STRONG>, ADO lee la propiedad <STRONG>Value</STRONG> solo una vez desde el proveedor. Si un comando incluye un objeto <STRONG>Parameter</STRONG> cuya propiedad <STRONG>Value</STRONG> está vacía y se crea un objeto <A href="recordset-object-ado.md">Recordset</A> a partir del comando, asegúrese de cerrar <STRONG>Recordset</STRONG> antes de recuperar la propiedad <STRONG>Value</STRONG>. De lo contrario, para algunos proveedores, la propiedad <STRONG>Value</STRONG> puede estar vacía y no contendrá el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="d8fd1-p103">For <STRONG>Parameter</STRONG> objects, ADO reads the <STRONG>Value</STRONG> property only once from the provider. If a command contains a <STRONG>Parameter</STRONG> whose <STRONG>Value</STRONG> property is empty, and you create a <A href="recordset-object-ado.md">Recordset</A> from the command, ensure that you first close the <STRONG>Recordset</STRONG> before retrieving the <STRONG>Value</STRONG> property. Otherwise, for some providers, the <STRONG>Value</STRONG> property may be empty, and won't contain the correct value.</span></span></P>



<span data-ttu-id="d8fd1-p104">En los nuevos objetos **Field** que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), es necesario establecer la propiedad **Value** antes de especificar cualquier otra propiedad **Field**. En primer lugar, debe haberse asignado un valor específico a la propiedad **Value** y se debe haber llamado al método [Update](update-method-ado.md) de la colección **Fields**. A continuación, será posible obtener acceso a otras propiedades como [Type](type-property-ado.md) o [Attributes](attributes-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d8fd1-p104">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>


---
title: CommandText (propiedad, ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 66797accb24cead7d7ba5732f0a9c58ee31049e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296139"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="d5ed7-102">CommandText (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d5ed7-102">CommandText property (ADO)</span></span>


<span data-ttu-id="d5ed7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5ed7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5ed7-104">Indica el texto de un comando que se va a emitir en un proveedor.</span><span class="sxs-lookup"><span data-stu-id="d5ed7-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d5ed7-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="d5ed7-105">Settings and return values</span></span>

<span data-ttu-id="d5ed7-p101">Establece o devuelve un valor de tipo **String** que contiene un comando de proveedor, como una instrucción SQL, un nombre de tabla, una dirección URL relativa o una llamada a un procedimiento almacenado. El valor predeterminado es "" (cadena de longitud cero).</span><span class="sxs-lookup"><span data-stu-id="d5ed7-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ed7-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5ed7-108">Remarks</span></span>

<span data-ttu-id="d5ed7-p102">Utilice la propiedad **CommandText** para establecer o devolver el texto de un comando representado por un objeto [Command](command-object-ado.md). Normalmente es una instrucción SQL, pero también puede ser cualquier otro tipo de instrucción de comando que reconozca el proveedor, como una llamada a un procedimiento almacenado. El procesador de consultas del proveedor debe admitir el dialecto o la versión de la instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="d5ed7-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="d5ed7-112">Si la propiedad [Prepared](prepared-property-ado.md) del objeto **Command** tiene el valor **True** y el objeto **Command** está enlazado a una conexión abierta cuando se establece el valor de la propiedad **CommandText**, ADO preparará la consulta (es decir, una forma compilada de la consulta que el proveedor almacena) cuando se llame a los métodos [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) u **Open**.</span><span class="sxs-lookup"><span data-stu-id="d5ed7-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) or **Open** methods.</span></span>

<span data-ttu-id="d5ed7-p103">Dependiendo del valor de la propiedad [CommandType](commandtype-property-ado.md), puede que ADO modifique la propiedad **CommandText**. La propiedad **CommandText** se puede leer en cualquier momento para ver el texto real del comando que ADO va a utilizar durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="d5ed7-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="d5ed7-p104">Utilice la propiedad **CommandText** para establecer o devolver una dirección URL relativa que especifica un recurso, como un archivo o un directorio. El recurso es relativo a una ubicación especificada explícitamente por una dirección URL absoluta o implícitamente por un objeto [Connection](connection-object-ado.md) abierto.</span><span class="sxs-lookup"><span data-stu-id="d5ed7-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <span data-ttu-id="d5ed7-117">[!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="d5ed7-117">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="d5ed7-118">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="d5ed7-118">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>



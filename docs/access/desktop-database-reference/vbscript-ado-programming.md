---
title: Programación ADO en VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4aff2c8b3394321367851ad82e4e7efe98badff8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306030"
---
# <a name="vbscript-ado-programming"></a><span data-ttu-id="cd641-102">Programación de ADO con VBScript</span><span class="sxs-lookup"><span data-stu-id="cd641-102">VBScript ADO programming</span></span>


<span data-ttu-id="cd641-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd641-103">**Applies to**: Access 2013, Office 2013</span></span> 

## <a name="creating-an-ado-project"></a><span data-ttu-id="cd641-104">Crear un proyecto de ADO</span><span class="sxs-lookup"><span data-stu-id="cd641-104">Creating an ADO Project</span></span>

<span data-ttu-id="cd641-p101">Microsoft Visual Basic Scripting Edition no admite bibliotecas de tipos, de modo que no es necesario hacer referencia a ADO en su proyecto. En consecuencia, no se admite ninguna característica asociada, tal como la finalización de línea de comando. Además, de forma predeterminada, las constantes enumeradas de ADO no se encuentran definidas en VBScript.</span><span class="sxs-lookup"><span data-stu-id="cd641-p101">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in VBScript.</span></span>

<span data-ttu-id="cd641-108">Sin embargo, ADO proporciona dos archivos de inclusión que contienen las siguientes definiciones utilizadas con VBScript:</span><span class="sxs-lookup"><span data-stu-id="cd641-108">However, ADO provides you with two include files containing the following definitions to be used with VBScript:</span></span>

  - <span data-ttu-id="cd641-109">Para scripting del lado servidor, use Adovbs.inc, que está instalado en la carpeta c: Archivos de programa common \\ \\ Files System \\ \\ ado de forma \\ predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cd641-109">For server-side scripting use Adovbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

  - <span data-ttu-id="cd641-110">Para scripting del lado cliente, use Adcvbs.inc, que está instalado en la carpeta \\ \\ \\ \\ msdac del sistema de archivos comunes de archivos de programa c: \\ de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cd641-110">For client-side scripting use Adcvbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="cd641-111">Puede copiar y pegar definiciones de constantes de estos archivos en sus páginas ASP o, si está realizando scripting del lado servidor, copie el archivo Adovbs.inc en una carpeta del sitio web y haciendo referencia a él desde la página ASP de esta forma:</span><span class="sxs-lookup"><span data-stu-id="cd641-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your website and referencing it from your ASP page like this:</span></span>

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a><span data-ttu-id="cd641-112">Crear objetos de ADO en VBScript</span><span class="sxs-lookup"><span data-stu-id="cd641-112">Creating ADO Objects in VBScript</span></span>

<span data-ttu-id="cd641-p102">No es posible utilizar la instrucción **Dim** para asignar objetos a un tipo específico en VBScript. Además, VBScript no admite la sintaxis **New** utilizada con la instrucción **Dim** en Visual Basic para Aplicaciones (VBA). Deberá utilizar la llamada a la función **CreateObject**:</span><span class="sxs-lookup"><span data-stu-id="cd641-p102">You cannot use the **Dim** statement to assign objects to a specific type in VBScript. Also, VBScript does not support the **New** syntax used with the **Dim** statement in Visual Basic for Applications. You must instead use the **CreateObject** function call:</span></span>

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a><span data-ttu-id="cd641-116">Ejemplos de VBScript</span><span class="sxs-lookup"><span data-stu-id="cd641-116">VBScript Examples</span></span>

<span data-ttu-id="cd641-117">El código siguiente es un ejemplo genérico de programación de servidor con VBScript en un archivo ASP:</span><span class="sxs-lookup"><span data-stu-id="cd641-117">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</span></span>

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

<span data-ttu-id="cd641-118">En la documentación de ADO, se incluyen ejemplos más específicos de VBScript.</span><span class="sxs-lookup"><span data-stu-id="cd641-118">More specific VBScript examples are included with the ADO documentation.</span></span> <span data-ttu-id="cd641-119">Para obtener más información, vea [ejemplos de código de ADO en Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span><span class="sxs-lookup"><span data-stu-id="cd641-119">For more information, see [ADO code examples in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span></span>

## <a name="differences-between-vbscript-and-visual-basic"></a><span data-ttu-id="cd641-120">Diferencias entre VBScript y Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cd641-120">Differences Between VBScript and Visual Basic</span></span>

<span data-ttu-id="cd641-p104">El uso de ADO con VBScript es similar al uso con Visual Basic, incluido el uso de la sintaxis. Sin embargo, existen algunas diferencias significativas:</span><span class="sxs-lookup"><span data-stu-id="cd641-p104">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used. However, some significant differences exist:</span></span>

- <span data-ttu-id="cd641-p105">VBScript sólo admite el tipo de datos Variant, el cual puede contener diferentes tipos de datos. Es posible almacenar los datos que se necesitan en un tipo de datos Variant, y aquéllos funcionarán correctamente debido a la conversión realizada por VBScript. Éste reconoce el tipo requerido por ADO y convierte el valor correspondiente del Variant en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="cd641-p105">VBScript supports only the Variant data type, which can hold different types of data. You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript. It recognizes the type required by ADO, and converts the value in the Variant accordingly.</span></span>

- <span data-ttu-id="cd641-126">No se puede `on error goto <label>` usar en VBScript.</span><span class="sxs-lookup"><span data-stu-id="cd641-126">You cannot use `on error goto <label>` within VBScript.</span></span>

- <span data-ttu-id="cd641-p106">VBScript admite algunas de las funciones incorporadas de Visual Basic, tales como **Msgbox**, **Date** y **IsNumeric**. Sin embargo, puesto que VBScript es un subconjunto de Visual Basic, no todas las funciones integradas están admitidas. Por ejemplo, VBScript no admite la función **Format** ni las funciones de E/S de archivo.</span><span class="sxs-lookup"><span data-stu-id="cd641-p106">VBScript supports some of the built-in Visual Basic functions such as **Msgbox**, **Date**, and **IsNumeric**. However, because VBScript is a subset of Visual Basic, not all built-in functions are supported. For example, VBScript does not support the **Format** function and the file I/O functions.</span></span>


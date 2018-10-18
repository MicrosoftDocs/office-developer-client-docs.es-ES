---
title: Tutorial de RDS (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d87dc84217b716505302464825a1857fecf67669
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606825"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="01f26-102">Tutorial de RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="01f26-102">RDS Tutorial (VBScript)</span></span>


<span data-ttu-id="01f26-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="01f26-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="01f26-p101">Éste es el Tutorial de RDS, escrito en Microsoft Visual Basic Scripting Edition. Para obtener una descripción del propósito de este tutorial, vea [Tutorial de RDS](chapter-12-rds-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="01f26-p101">This is the RDS Tutorial, written in Microsoft Visual Basic Scripting Edition. For a description of the purpose of this tutorial, see the [RDS Tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="01f26-106">En este tutorial, [RDS. DataControl](datacontrol-object-rds.md) y [RDS. DataSpace](dataspace-object-rds.md) se crean en tiempo de diseño, es decir, se definen con etiquetas de objeto como ésta:.</span><span class="sxs-lookup"><span data-stu-id="01f26-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time — that is, they are defined with object tags, like this: .</span></span> <span data-ttu-id="01f26-107">De forma alternativa, se podrían crear en tiempo de ejecución con el método **Server.CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="01f26-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> <span data-ttu-id="01f26-108">Por ejemplo, el objeto **RDS.DataControl** se crearía del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="01f26-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

<span data-ttu-id="01f26-109">**Paso 1 : Especificar un programa de servidor**</span><span class="sxs-lookup"><span data-stu-id="01f26-109">**Step 1 — Specify a server program**</span></span>

<span data-ttu-id="01f26-110"><<<<<<< HEAD VBScript puede descubrir el nombre del servidor Web de IIS se está ejecutando mediante el método **Request.ServerVariables** de VBScript disponible para páginas Active Server: === VBScript puede descubrir el nombre del sitio web IIS servidor que se ejecuta mediante el método **Request.ServerVariables** de VBScript disponible para páginas Active Server:</span><span class="sxs-lookup"><span data-stu-id="01f26-110"><<<<<<< HEAD VBScript can discover the name of the IIS Web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages: ======= VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>
>>>>>>> <span data-ttu-id="01f26-111">master</span><span class="sxs-lookup"><span data-stu-id="01f26-111">master</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="01f26-112">Sin embargo, para este tutorial, utilice el servidor imaginario "yourServer".</span><span class="sxs-lookup"><span data-stu-id="01f26-112">However, for this tutorial, use the imaginary server, "yourServer".</span></span>


> [!NOTE]
> <P><span data-ttu-id="01f26-p103">[!NOTA] Preste atención a los tipos de datos de argumentos <STRONG>ByRef</STRONG>. VBScript no permite especificar el tipo de variable, por lo que siempre se debe pasar un tipo Variant. Cuando se usa HTTP, RDS permitirá pasar un valor Variant a un método que espera un valor no Variant si lo llama con el método <STRONG>CreateObject</STRONG> del objeto <A href="createobject-method-rds.md">RDS.DataSpace</A>. Cuando se usa DCOM o un servidor en proceso, use los mismos tipos de parámetro en el cliente y en el servidor o recibirá un error de no coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="01f26-p103">Pay attention to the data type of <STRONG>ByRef</STRONG> arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <STRONG>RDS.DataSpace</STRONG> object <A href="createobject-method-rds.md">CreateObject</A> method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span></P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

<span data-ttu-id="01f26-117">**Paso 2a : Llamar al programa de servidor con RDS.DataControl**</span><span class="sxs-lookup"><span data-stu-id="01f26-117">**Step 2a — Invoke the server program with RDS.DataControl**</span></span>

<span data-ttu-id="01f26-118">Este ejemplo es simplemente un comentario que muestra que el comportamiento predeterminado del objeto **RDS.DataControl** consiste en realizar la consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="01f26-118">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="01f26-119">**Paso 2b : Llamar al programa servidor con RDSServer.DataFactory**</span><span class="sxs-lookup"><span data-stu-id="01f26-119">**Step 2b — Invoke the server program with RDSServer.DataFactory**</span></span>

<span data-ttu-id="01f26-120">**Paso 3 : El servidor obtiene un objeto Recordset**</span><span class="sxs-lookup"><span data-stu-id="01f26-120">**Step 3 — Server obtains a Recordset**</span></span>

<span data-ttu-id="01f26-121">**Paso 4 : El servidor devuelve un objeto Recordset**</span><span class="sxs-lookup"><span data-stu-id="01f26-121">**Step 4 — Server returns the Recordset**</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

<span data-ttu-id="01f26-122">**Paso 5 : El uso de DataControl se facilita mediante controles visuales**</span><span class="sxs-lookup"><span data-stu-id="01f26-122">**Step 5 — DataControl is made usable by visual controls**</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

<span data-ttu-id="01f26-123">**Paso 6a : Los cambios se envían al servidor con RDS.DataControl**</span><span class="sxs-lookup"><span data-stu-id="01f26-123">**Step 6a — Changes are sent to the server with RDS.DataControl**</span></span>

<span data-ttu-id="01f26-124">Este ejemplo es simplemente un comentario que demuestra cómo el objeto **RDS.DataControl** realiza las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="01f26-124">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

<span data-ttu-id="01f26-125">**Paso 6b : Los cambios se envían al servidor con RDSServer.DataFactory**</span><span class="sxs-lookup"><span data-stu-id="01f26-125">**Step 6b — Changes are sent to the server with RDSServer.DataFactory**</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="01f26-126">**Éste es el final del tutorial.**</span><span class="sxs-lookup"><span data-stu-id="01f26-126">**This is the end of the tutorial.**</span></span>


---
title: Tutorial de RDS (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 996c0adf8c883de5c73174d726cf5bd11fc42457
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996884"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="ee93c-102">Tutorial de RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="ee93c-102">RDS tutorial (VBScript)</span></span>

<span data-ttu-id="ee93c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee93c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee93c-104">Este es el tutorial de RDS, escrito en Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="ee93c-104">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="ee93c-105">Para obtener una descripción del propósito de este tutorial, vea el [tutorial de RDS](chapter-12-rds-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="ee93c-105">For a description of the purpose of this tutorial, see the [RDS tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="ee93c-106">En este tutorial, [RDS. DataControl](datacontrol-object-rds.md) y [RDS. DataSpace](dataspace-object-rds.md) se crean en tiempo de diseño; es decir, se definen con etiquetas de objeto.</span><span class="sxs-lookup"><span data-stu-id="ee93c-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="ee93c-107">De forma alternativa, se podrían crear en tiempo de ejecución con el método **Server.CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="ee93c-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="ee93c-108">Por ejemplo, el objeto **RDS.DataControl** se crearía del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="ee93c-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

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

## <a name="step-1--specify-a-server-program"></a><span data-ttu-id="ee93c-109">Paso 1 : Especificar un programa de servidor</span><span class="sxs-lookup"><span data-stu-id="ee93c-109">Step 1 — Specify a server program</span></span>

<span data-ttu-id="ee93c-110">VBScript puede descubrir el nombre del servidor web IIS que se está ejecutando mediante el método **Request.ServerVariables** de VBScript disponible para páginas Active Server:</span><span class="sxs-lookup"><span data-stu-id="ee93c-110">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="ee93c-111">Sin embargo, para este tutorial, utilice el servidor imaginario "yourServer".</span><span class="sxs-lookup"><span data-stu-id="ee93c-111">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="ee93c-p103">[!NOTA] Preste atención a los tipos de datos de argumentos **ByRef**. VBScript no permite especificar el tipo de variable, por lo que siempre se debe pasar un tipo Variant. Cuando se usa HTTP, RDS permitirá pasar un valor Variant a un método que espera un valor no Variant si lo llama con el método **CreateObject** del objeto [RDS.DataSpace](createobject-method-rds.md). Cuando se usa DCOM o un servidor en proceso, use los mismos tipos de parámetro en el cliente y en el servidor o recibirá un error de no coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="ee93c-p103">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="ee93c-116">Paso 2a : Llamar al programa de servidor con RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="ee93c-116">Step 2a — Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="ee93c-117">Este ejemplo es simplemente un comentario que muestra que el comportamiento predeterminado del objeto **RDS.DataControl** consiste en realizar la consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="ee93c-117">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

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

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a><span data-ttu-id="ee93c-118">Paso 2b : Llamar al programa servidor con RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee93c-118">Step 2b — Invoke the server program with RDSServer.DataFactory</span></span>

## <a name="step-3--server-obtains-a-recordset"></a><span data-ttu-id="ee93c-119">Paso 3 : El servidor obtiene un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="ee93c-119">Step 3 — Server obtains a Recordset</span></span>

## <a name="step-4--server-returns-the-recordset"></a><span data-ttu-id="ee93c-120">Paso 4 : El servidor devuelve un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="ee93c-120">Step 4 — Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="ee93c-121">Paso 5 : El uso de DataControl se facilita mediante controles visuales</span><span class="sxs-lookup"><span data-stu-id="ee93c-121">Step 5 — DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="ee93c-122">Paso 6a: los cambios se envían al servidor con RDS. DataControl \*</span><span class="sxs-lookup"><span data-stu-id="ee93c-122">Step 6a — Changes are sent to the server with RDS.DataControl\*</span></span>

<span data-ttu-id="ee93c-123">Este ejemplo es simplemente un comentario que demuestra cómo el objeto **RDS.DataControl** realiza las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="ee93c-123">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

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

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="ee93c-124">Paso 6b : Los cambios se envían al servidor con RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee93c-124">Step 6b — Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="ee93c-125">**Éste es el final del tutorial.**</span><span class="sxs-lookup"><span data-stu-id="ee93c-125">**This is the end of the tutorial.**</span></span>


---
title: Escenario de publicación en Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f481c4bc5cf11f9345458b3859c099b40a79885
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026452"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="3a3ad-102">Escenario de publicación en Internet</span><span class="sxs-lookup"><span data-stu-id="3a3ad-102">Internet publishing scenario</span></span>

<span data-ttu-id="3a3ad-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a3ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a3ad-p101">En este ejemplo de código, se muestra cómo usar ADO con Microsoft OLE DB Provider for Internet Publishing. En este escenario, creará una aplicación de Visual Basic que usa objetos **Recordset**, **Record** y **Stream** para mostrar el contenido de recursos publicados con el proveedor de publicaciones en Internet.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-p101">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing. In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="3a3ad-106">Para crear el escenario, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3a3ad-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="3a3ad-107">Configurar el proyecto de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="3a3ad-108">Inicializar el cuadro de lista principal.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="3a3ad-109">Rellenar el cuadro de lista de campos.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="3a3ad-110">Rellenar el cuadro de texto de detalles.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="3a3ad-111">Paso 1: Configurar el proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3a3ad-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="3a3ad-112">En este escenario, se supone que han instalado Microsoft Visual Basic 6.0 y ADO 2.5, o versiones posteriores, y Microsoft OLE DB Provider for Internet Publishing en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="3a3ad-113">Crear un proyecto de ADO</span><span class="sxs-lookup"><span data-stu-id="3a3ad-113">Create an ADO project</span></span>

1.  <span data-ttu-id="3a3ad-114">En Microsoft Visual Basic, cree un nuevo proyecto EXE estándar.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="3a3ad-115">En el menú **Herramientas**, haga clic en **Referencias**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="3a3ad-116">Seleccione la **Biblioteca Microsoft ActiveX Data Objects 2.5**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="3a3ad-117">Insertar controles en el formulario principal</span><span class="sxs-lookup"><span data-stu-id="3a3ad-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="3a3ad-118">Agregue un control ListBox a Form1.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="3a3ad-119">Establezca su propiedad **Name** en **lstMain**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="3a3ad-120">Agregue otro control ListBox a Form1.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="3a3ad-121">Establezca su propiedad **Name** en **lstDetails**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="3a3ad-122">Agregue un control TextBox a Form1.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="3a3ad-123">Establezca su propiedad **Name** en **txtDetails**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="3a3ad-124">Paso 2: Inicializar el cuadro de lista principal</span><span class="sxs-lookup"><span data-stu-id="3a3ad-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="3a3ad-125">Declarar objetos Record y Recordset globales</span><span class="sxs-lookup"><span data-stu-id="3a3ad-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="3a3ad-126">Inserte el código siguiente en la sección de declaraciones generales de Form1:</span><span class="sxs-lookup"><span data-stu-id="3a3ad-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="3a3ad-127">Este código declara referencias de objetos globales para **Record** y **Recordset** que se usarán posteriormente en este escenario.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="3a3ad-128">Conectarse a una dirección URL y llenar lstMain</span><span class="sxs-lookup"><span data-stu-id="3a3ad-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="3a3ad-129">Inserte el código siguiente en el controlador del evento Form Load para Form1:</span><span class="sxs-lookup"><span data-stu-id="3a3ad-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   <span data-ttu-id="3a3ad-130">Este código crea instancias de los objetos globales **Record** y **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="3a3ad-131">El **registro** `grec` se abre con una dirección URL especificada como **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="3a3ad-132">Si la dirección URL existe, se abre; si aún no existe, se crea.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="3a3ad-133">Tenga en cuenta que se debe reemplazar `https://servername/foldername/` con una dirección URL válida de su entorno.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="3a3ad-134">El **objeto Recordset** `grs` se abre sobre los elementos secundarios del **registro** `grec`.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="3a3ad-135">El lstMain, a continuación, se rellena con los nombres de archivo de los recursos publicados en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="3a3ad-136">Paso 3: Rellenar el cuadro de lista de campos</span><span class="sxs-lookup"><span data-stu-id="3a3ad-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="3a3ad-137">Inserte el siguiente código en el controlador del evento Click de lstMain:</span><span class="sxs-lookup"><span data-stu-id="3a3ad-137">Insert the following code into the Click event handler of lstMain:</span></span>

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   <span data-ttu-id="3a3ad-138">Este código declara y crea instancias de objetos **Record** y **Recordset** locales `rec` y `rs`respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="3a3ad-139">La fila correspondiente al recurso seleccionado en lstMain se convierte en la fila actual de `grs`.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="3a3ad-140">A continuación, se borra el cuadro de lista **Detalles** y `rec` se abre con la fila actual de `grs` como el origen.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="3a3ad-141">Si el recurso es un registro de colección (según se especifica en **RecordType**), el **conjunto de registros** de local `rs` se abre sobre los elementos secundarios de `rec`.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="3a3ad-142">a continuación, se rellena lstDetails con los valores de las filas de `rs`.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="3a3ad-143">Si el recurso es un registro simple, `recFields` se llama.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="3a3ad-144">Para obtener más información acerca de `recFields`, vea el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="3a3ad-145">Si el recurso es un documento estructurado, entonces no se implementa ningún código.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="3a3ad-146">Paso 4: Rellenar el cuadro de texto de detalles</span><span class="sxs-lookup"><span data-stu-id="3a3ad-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="3a3ad-147">Cree una subrutina nueva denominada `recFields` e inserte el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a3ad-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   <span data-ttu-id="3a3ad-148">Este código rellena lstDetails con los campos y valores del registro simple pasan a `recFields`.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="3a3ad-149">Si el recurso es un archivo de texto, se abre un **Stream** de texto desde el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="3a3ad-150">El código determina si el juego de caracteres es ASCII y copia el contenido de la **secuencia** en `txtDetails`.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>


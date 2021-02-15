---
title: Escenario de publicación en Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291275"
---
# <a name="internet-publishing-scenario"></a>Escenario de publicación en Internet

**Se aplica a:** Access 2013, Office 2013

En este ejemplo de código, se muestra cómo usar ADO con Microsoft OLE DB Provider for Internet Publishing. En este escenario, creará una aplicación de Visual Basic que usa objetos **Recordset**, **Record** y **Stream** para mostrar el contenido de recursos publicados con el proveedor de publicaciones en Internet.

Para crear el escenario, siga estos pasos: 

1. Configure el proyecto Visual Basic proyecto.
2. Inicializar el cuadro de lista Principal.
3. Rellene el cuadro de lista Campos.
4. Rellene el cuadro de texto Detalles.

## <a name="step-1-set-up-the-visual-basic-project"></a>Paso 1: Configurar el proyecto Visual Basic proyecto

En este escenario, se supone que han instalado Microsoft Visual Basic 6.0 y ADO 2.5, o versiones posteriores, y Microsoft OLE DB Provider for Internet Publishing en el sistema.

### <a name="create-an-ado-project"></a>Crear un proyecto de ADO

1.  En Microsoft Visual Basic, cree un nuevo proyecto EXE estándar.

2.  En el menú **Herramientas**, haga clic en **Referencias**.

3.  Seleccione **Microsoft ActiveX Biblioteca de objetos de datos 2.5** y, a continuación, haga clic en **Aceptar**.

### <a name="insert-controls-on-the-main-form"></a>Insertar controles en el formulario principal

1.  Agregue un control ListBox a Form1. Establezca su **propiedad Name** en **lstMain**.

2.  Agregue otro control ListBox a Form1. Establezca su **propiedad Name** en **lstDetails**.

3.  Agregue un control TextBox a Form1. Establezca su **propiedad Name** en **txtDetails**.

## <a name="step-2-initialize-the-main-list-box"></a>Paso 2: Inicializar el cuadro de lista Principal

### <a name="declare-global-record-and-recordset-objects"></a>Declarar objetos Record y Recordset globales

- Inserte el código siguiente en la sección de declaraciones generales de Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Este código declara referencias de objetos globales para **Record** y **Recordset** que se usarán posteriormente en este escenario.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Conectarse a una dirección URL y rellenar lstMain

- Inserte el código siguiente en el controlador del evento Form Load para Form1:
    
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
    
   Este código crea instancias de los objetos globales **Record** y **Recordset**. El **registro** `grec` se abre con una dirección URL especificada como **ActiveConnection**. Si la dirección URL existe, se abre; si aún no existe, se crea. 
   
   Tenga en cuenta que debe reemplazar `https://servername/foldername/` con una dirección URL válida de su entorno. 
   
   El **conjunto de** registros se abre en los objetos secundarios del objeto `grs` **Record** `grec` . A continuación, lstMain se rellena con los nombres de archivo de los recursos publicados en la dirección URL.

## <a name="step-3-populate-the-fields-list-box"></a>Paso 3: Rellenar el cuadro de lista Campos

- Inserte el siguiente código en el controlador del evento Click de lstMain:

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

   Este código declara y crea instancias de los objetos **Locales Record** y **Recordset,** `rec` `rs` respectivamente.

   La fila correspondiente al recurso seleccionado en lstMain se ha hecho la fila actual de `grs` . A **continuación,** se borra el cuadro de lista Detalles y se abre `rec` con la fila actual como `grs` origen.

   Si el recurso es un registro de colección (especificado por **RecordType**), el conjunto de registros **local** `rs` se abre en los elementos secundarios de `rec` . lstDetails, a continuación, se rellena con los valores de las filas de `rs` .

   Si el recurso es un registro simple, `recFields` se llama. Para obtener más información `recFields` acerca de , vea el siguiente paso.

   Si el recurso es un documento estructurado, entonces no se implementa ningún código.

## <a name="step-4-populate-the-details-text-box"></a>Paso 4: Rellenar el cuadro de texto Detalles

- Cree una subrutina con nombre `recFields` e inserte el código siguiente:

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

   Este código rellena lstDetails con los campos y valores del registro simple pasado a `recFields` . Si el recurso es un archivo de texto, se abre un **Stream** de texto a partir del registro. El código determina si el juego de caracteres es ASCII y copia el contenido **de stream** en `txtDetails` .


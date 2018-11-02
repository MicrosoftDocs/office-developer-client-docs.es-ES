---
title: Field2.SaveToFile (método) (DAO)
TOCTitle: SaveToFile Method
ms:assetid: 250f9596-1a03-471d-96f9-718cd57dc94f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191852(v=office.15)
ms:contentKeyID: 48543776
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101191
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c73aa8f4023ea5d3a192608fad88bf336e6e858f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924802"
---
# <a name="field2savetofile-method-dao"></a><span data-ttu-id="8ecd9-102">Field2.SaveToFile (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="8ecd9-102">Field2.SaveToFile method (DAO)</span></span>

<span data-ttu-id="8ecd9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ecd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ecd9-104">Guarda un archivo adjunto en el disco.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-104">Saves an attachment to disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="8ecd9-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="8ecd9-105">Version Information</span></span>

<span data-ttu-id="8ecd9-106">Versión añadida: Access 2007</span><span class="sxs-lookup"><span data-stu-id="8ecd9-106">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="8ecd9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ecd9-107">Syntax</span></span>

<span data-ttu-id="8ecd9-108">*expresión* . SaveToFile (***FileName***)</span><span class="sxs-lookup"><span data-stu-id="8ecd9-108">*expression* .SaveToFile(***FileName***)</span></span>

<span data-ttu-id="8ecd9-109">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="8ecd9-109">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8ecd9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ecd9-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ecd9-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ecd9-111">Name</span></span></p></th>
<th><p><span data-ttu-id="8ecd9-112">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="8ecd9-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8ecd9-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8ecd9-113">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8ecd9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ecd9-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ecd9-115">FileName</span><span class="sxs-lookup"><span data-stu-id="8ecd9-115">FileName</span></span></p></td>
<td><p><span data-ttu-id="8ecd9-116">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8ecd9-116">Required</span></span></p></td>
<td><p><span data-ttu-id="8ecd9-117"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8ecd9-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8ecd9-118">Ruta de acceso completa del archivo en el que desea guardar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-118">The fully qualified path of the file to which you want to save the attachment.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="8ecd9-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ecd9-119">Example</span></span>

<span data-ttu-id="8ecd9-120">El siguiente fragmento de código ilustra cómo utilizar el método **SaveToFile** para guardar todos los datos adjuntos de un empleado determinado en el disco.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-120">The following code snippet illustrates how to use the **SaveToFile** method to save all of the attachments for a specific employee to disk.</span></span>

```vb
    '  Instantiate the parent recordset.  
       Set rsEmployees = db.OpenRecordset("Employees") 
      
       … Code to move to desired employee 
      
       ' Instantiate the child recordset. 
       Set rsPictures = rsEmployees.Fields("Pictures").Value  
     
       '  Loop through the attachments. 
       While Not rsPictures.EOF 
      
          '  Save current attachment to disk in the "My Documents" folder. 
          rsPictures.Fields("FileData").SaveToFile _ 
                      "C:\Documents and Settings\Username\My Documents" 
          rsPictures.MoveNext 
       Wend 
```

<br/>

<span data-ttu-id="8ecd9-121">En el ejemplo siguiente se muestra cómo guardar los archivos almacenados en un campo de datos adjuntos a la ruta de acceso de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="8ecd9-121">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

<span data-ttu-id="8ecd9-122">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8ecd9-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Function SaveAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        Dim strFullPath As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Save all attachments in the field
            Do While Not rsA.EOF
                If rsA("FileName") Like strPattern Then
                    strFullPath = strPath & "\" & rsA("FileName")
                    
                    'Make sure the file does not exist and save
                    If Dir(strFullPath) = "" Then
                        rsA("FileData").SaveToFile strFullPath
                    End If
                    
                    'Increment the number of files saved
                    SaveAttachments = SaveAttachments + 1
                End If
                
                'Next attachment
                rsA.MoveNext
            Loop
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

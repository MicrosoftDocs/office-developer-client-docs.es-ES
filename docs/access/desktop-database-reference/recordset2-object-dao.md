---
title: Objeto Recordset2 (DAO)
TOCTitle: Recordset2 Object
ms:assetid: 964f9961-807c-e4f3-5919-74e25f6e9069
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197737(v=office.15)
ms:contentKeyID: 48546446
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e4ab089af54a53889afac054598cbca57028353
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924683"
---
# <a name="recordset2-object-dao"></a><span data-ttu-id="aab1d-102">Objeto Recordset2 (DAO)</span><span class="sxs-lookup"><span data-stu-id="aab1d-102">Recordset2 object (DAO)</span></span>

<span data-ttu-id="aab1d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aab1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aab1d-104">Un objeto **Recordset2** representa los registros de una tabla base o los registros resultantes de la ejecución de una consulta.</span><span class="sxs-lookup"><span data-stu-id="aab1d-104">A **Recordset2** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="aab1d-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aab1d-105">Remarks</span></span>

<span data-ttu-id="aab1d-p101">Un objeto **Recordset2** contiene las mismas propiedades y métodos que el objeto **[Recordset](recordset-object-dao.md)**. El objeto **Recordset2** contiene una propiedad nueva, **[ParentRecordset](recordset2-parentrecordset-property-dao.md)**, que admite tipos de campo multivalor.</span><span class="sxs-lookup"><span data-stu-id="aab1d-p101">A **Recordset2** object is contains all of the same properties and methods as the **[Recordset](recordset-object-dao.md)** object. The **Recordset2** object contains a new property, **[ParentRecordset](recordset2-parentrecordset-property-dao.md)**, that support multi-valued field types.</span></span>

## <a name="example"></a><span data-ttu-id="aab1d-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aab1d-108">Example</span></span>

<span data-ttu-id="aab1d-109">En el ejemplo siguiente se muestra cómo desplazarse por un conjunto de registros que contiene un campo multivalor.</span><span class="sxs-lookup"><span data-stu-id="aab1d-109">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="aab1d-110">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="aab1d-110">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub PrintStudentsAndClasses()
        Dim dbs As DAO.Database
        Dim rsStudents As DAO.Recordset2  'Recordset for students
        Dim rsClasses As DAO.Recordset2  'Recordset for classes
        Dim fld As DAO.Field2
    
        'open the database
        Set dbs = CurrentDb()
    
        'get the table of students
        Set rsStudents = dbs.OpenRecordset("tblStudents")
    
        'loop through the students
        Do While Not rsStudents.EOF
            
            'get the classes field
            Set fld = rsStudents("Classes")
    
            'get the classes Recordset
            'make sure the field is a multi-valued field before
            'getting a Recordset object
            If fld.IsComplex Then
                Set rsClasses = fld.Value
            End If
    
            'access all records in the Recordset
            If Not (rsClasses.BOF And rsClasses.EOF) Then
                rsClasses.MoveLast
                rsClasses.MoveFirst
            End If
    
            'print the student and number of classes
            Debug.Print rsStudents("FirstName") & " " & rsStudents("LastName"), _
                "Number of classes: " & rsClasses.RecordCount
    
            'print the classes for this student
            Do While Not rsClasses.EOF
                Debug.Print , rsClasses("Value")
                rsClasses.MoveNext
            Loop
    
            'close the Classes Recordset
            rsClasses.Close
    
            'get the next student
            rsStudents.MoveNext
    
        Loop
        
        'cleanup
        rsStudents.Close
    
        Set fld = Nothing
        Set rsStudents = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="aab1d-111">En el ejemplo siguiente se muestra cómo desplazarse por los archivos en un campo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="aab1d-111">The following example shows how to navigate the files in an attachment field.</span></span> <span data-ttu-id="aab1d-112">El tipo de archivo y el nombre de archivo de cada dato adjunto se imprime en la ventana Inmediato.</span><span class="sxs-lookup"><span data-stu-id="aab1d-112">The file type and filename of each attachment is printed in the Immediate window.</span></span>

```vb
    Sub ListAttachments()
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Print the first and last name
            Debug.Print rst("FirstName") & " " & rst("LastName")
            
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Print all attachments in the field
            Do While Not rsA.EOF
                Debug.Print , rsA("FileType"), rsA("FileName")
                
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
    End Sub
```

<br/>

<span data-ttu-id="aab1d-113">En el ejemplo siguiente se muestra cómo agregar archivos desde una ruta de acceso de la carpeta especificada para un campo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="aab1d-113">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

```vb
    Public Function LoadAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld  As DAO.Field2
        Dim strFile As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Load all attachments in the specified directory
            strFile = Dir(strPath & "\*.*")
            
            rst.Edit
            Do While Len(strFile) > 0
                'Add a new attachment that matches the pattern.
                'Pass "" to match all files.
                If strFile Like strPattern Then
                    rsA.AddNew
                    rsA("FileData").LoadFromFile strPath & "\" & strFile
                    rsA.Update
                    
                    'Increment the number of files added
                    LoadAttachments = LoadAttachments + 1
                End If
                strFile = Dir
            Loop
            rsA.Close
            
            rst.Update
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

<br/>

<span data-ttu-id="aab1d-114">En el ejemplo siguiente se muestra cómo guardar los archivos almacenados en un campo de datos adjuntos a la ruta de acceso de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="aab1d-114">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

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

<br/>

<span data-ttu-id="aab1d-115">En el ejemplo siguiente se muestra cómo eliminar un archivo almacenado en un campo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="aab1d-115">The following example shows how to delete a file stored in an attachment field.</span></span>

```vb
    Function RemoveAttachment(strRemoveFile As String, Optional strFilter As String) As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database
        Set dbs = CurrentDb
        
        'Open the recordset. If the strFilter is supplied, add it to the WHERE
        'clause for the recordset. Otherwise, any files matching strFileName
        'will be deleted
        If Len(strFilter) > 0 Then
            Set rst = dbs.OpenRecordset("SELECT * FROM tblAttachments WHERE " & strFilter)
        Else
            Set rst = dbs.OpenRecordset("tblAttachments")
        End If
        
        'Get the Attachment field
        Set fld = rst("Attachments")
        
        'Navigate through the recordset
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Walk the attachments and look for the file name to remove
            Do While Not rsA.EOF
                If rsA("FileName") Like strRemoveFile Then
                    rsA.Delete
                    
                    'Increment the number of files removed
                    RemoveAttachment = RemoveAttachment + 1
                End If
                rsA.MoveNext
            Loop
                    
            'Cleanup the Attachments recordset
            rsA.Close
            Set rsA = Nothing
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        Set fld = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```


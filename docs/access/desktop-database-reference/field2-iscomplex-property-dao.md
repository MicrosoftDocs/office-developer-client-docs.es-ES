---
title: Field2.IsComplex Property (DAO)
TOCTitle: IsComplex Property
ms:assetid: ffc90e6e-e3ee-4f9b-ca6b-615199300d45
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837318(v=office.15)
ms:contentKeyID: 48548970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b7e5634256a3f0acf7dc058f36c5a7d9d0581b0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486022"
---
# <a name="field2iscomplex-property-dao"></a><span data-ttu-id="5b4b6-102">Field2.IsComplex Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="5b4b6-102">Field2.IsComplex Property (DAO)</span></span>

<span data-ttu-id="5b4b6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b4b6-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="5b4b6-p101">Devuelve un valor de tipo **Boolean** que indica si el campo especificado es un campo multivalor. Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-p101">Returns **Boolean** that indicates whether the specified field is a multi-valued data type. Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="5b4b6-106">Información de versión</span><span class="sxs-lookup"><span data-stu-id="5b4b6-106">Version information</span></span>

<span data-ttu-id="5b4b6-107">Versión añadida: Access 2007</span><span class="sxs-lookup"><span data-stu-id="5b4b6-107">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="5b4b6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b4b6-108">Syntax</span></span>

<span data-ttu-id="5b4b6-109">*expresión* . IsComplex</span><span class="sxs-lookup"><span data-stu-id="5b4b6-109">*expression* .IsComplex</span></span>

<span data-ttu-id="5b4b6-110">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="5b4b6-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="example"></a><span data-ttu-id="5b4b6-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b4b6-111">Example</span></span>

<span data-ttu-id="5b4b6-112">En el ejemplo siguiente se muestra cómo desplazarse por un conjunto de registros que contiene un campo multivalor.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-112">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="5b4b6-113">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="5b4b6-113">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

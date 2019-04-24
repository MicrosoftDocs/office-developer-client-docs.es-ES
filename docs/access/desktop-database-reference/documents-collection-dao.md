---
title: Colección Documents (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f6edd02c316fdff3f64b8a09c1504c46c9812a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293752"
---
# <a name="documents-collection-dao"></a>Colección Documents (DAO)


**Se aplica a:** Access 2013, Office 2013

Una colección **Documents** contiene todos los objetos **Document** de un tipo de objeto específico (solo bases de datos del motor de base de datos de Microsoft Access).

## <a name="remarks"></a>Comentarios

Cada objeto **Container** tiene una colección **Documents** que contiene objetos **Document** que describen instancias de objetos integrados del tipo especificado por el objeto **Container**.

Para hacer referencia a un objeto **Document** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

  - **Documents**(0)

  - **Documentos** ("*nombre*")

  - ****\!\[*Nombre* de los documentos\]

## <a name="example"></a>Ejemplo

En este ejemplo se enumera la colección **Documents** del contenedor Tables y, a continuación, se enumera la colección **Properties** del primer objeto **Document** de la colección.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```


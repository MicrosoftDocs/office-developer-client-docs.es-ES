---
title: Propiedad Document. Container (DAO)
TOCTitle: Container Property
ms:assetid: aa1ace1d-f0b8-e0b0-20b6-d3e296254c51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821451(v=office.15)
ms:contentKeyID: 48546940
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053320
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: af1a531e57aaca7d497f3f71d6c16e8ea1bab177
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293829"
---
# <a name="documentcontainer-property-dao"></a>Propiedad Document. Container (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve el nombre del objeto **[Container](container-object-dao.md)** al que pertenece un objeto **Document** (sólo áreas de trabajo de Microsoft Access). .

## <a name="syntax"></a>Sintaxis

*expresión* . Recipiente

*expresión* Variable que representa un objeto **Document** .

## <a name="example"></a>Ejemplo

En este ejemplo, se muestra la propiedad **Container** para diferentes objetos **Document**.

```vb 
Sub ContainerPropertyX() 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Display the container name for the first Document 
 ' object in each Container object's Documents collection. 
 For Each ctrLoop In dbsNorthwind.Containers 
 Debug.Print "Document: " & ctrLoop.Documents(0).Name 
 Debug.Print " Container = " & _ 
 ctrLoop.Documents(0).Container 
 Next ctrLoop 
 
 dbsNorthwind.Close 
 
End Sub 
 
```


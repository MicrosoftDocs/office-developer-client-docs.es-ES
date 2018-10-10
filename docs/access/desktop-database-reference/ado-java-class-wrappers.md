---
title: Contenedores de clase Java de ADO
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa3a4d1d2a917997b9e7ed5407d4f2ce8d1d0361
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485476"
---
# <a name="ado-java-class-wrappers"></a>Contenedores de clase Java de ADO


**Se aplica a**: Access 2013 | Office 2013

Este código declara una instancia del contenedor de clase [Recordset](recordset-object-ado.md) de ADO y lo inicializa, todo en la misma línea de código. Además, declara variables para cada uno de los argumentos del método [Open](open-method-ado-recordset.md), especialmente para [LockType](locktype-property-ado.md) y [CursorType](cursortype-property-ado.md) (porque Java no admite tipos enumerados). Abre y cierra el objeto **Recordset**. Al establecer Rs1 en NULL, simplemente se programa esa variable para que sea liberada cuando Java realice su liberación sistemática e intermitente de objetos no usados.

```java 
 
public static void main( String args[]) 
{ 
 msado15._Recordset Rs1 = new msado15.Recordset(); 
 Variant Source = new Variant( "SELECT * FROM Authors" ); 
 Variant Connect = new Variant( "DSN=AdoDemo;UID=admin;PWD=;" ); 
 int LockType = msado15.CursorTypeEnum.adOpenForwardOnly; 
 int CursorType = msado15.LockTypeEnum.adLockReadOnly; 
 int Options = -1; 
 
 Rs1.Open( Source, Connect, LockType, CursorType, Options ); 
 Rs1.Close(); 
 Rs1 = null; 
 
 System.out.println( "Success!\n" ); 
} 
```


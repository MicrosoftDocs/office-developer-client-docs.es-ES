---
title: Utilizar ADO con Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26eaa93a1abbb3778a2735d50dd5022edb3023d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306226"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Uso de ADO con Microsoft Visual Basic

**Se aplica a:** Access 2013, Office 2013

Configurar un proyecto de ADO y escribir código de ADO es un procedimiento similar en Visual Basic y Visual Basic para Aplicaciones. En este tema se aborda el uso de ADO con Visual Basic y Visual Basic para Aplicaciones, así como las diferencias.

## <a name="referencing-the-ado-library"></a>Referencia a la biblioteca de ADO

El proyecto debe hacer referencia a la biblioteca de ADO.

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>Para hacer referencia a ADO desde Microsoft Visual Basic

1. En Visual Basic, en el menú **Proyecto**, seleccione **Referencias**.

2. Seleccione **Biblioteca de Microsoft ActiveX Data Objects x.x** en la lista. Compruebe que estén seleccionadas al menos las siguientes bibliotecas:
   
   - Visual Basic para Aplicaciones
   - Objetos y procedimientos del motor en tiempo de ejecución de Visual Basic
   - Objetos y procedimientos de Visual Basic
   - Automatización OLE

3. Haga clic en **Aceptar**.

ADO se puede utilizar con la misma facilidad con Visual Basic para Aplicaciones mediante, por ejemplo, Microsoft Access.

### <a name="to-reference-ado-from-microsoft-access"></a>Para hacer referencia a ADO desde Microsoft Access

1. En Microsoft Access, seleccione o cree un módulo en la pestaña **Módulos** de la ventana **Base de datos**.

2. En el menú **Herramientas**, seleccione **Referencias**.

3. Seleccione **Biblioteca de Microsoft ActiveX Data Objects x.x** en la lista. Compruebe que estén seleccionadas al menos las siguientes bibliotecas:
    
   - Visual Basic para Aplicaciones
   - Biblioteca de objetos de Microsoft Access 11.0 (o posterior)

4. Haga clic en **Aceptar**.

## <a name="creating-ado-objects-in-visual-basic"></a>Creación de objetos de ADO en Visual Basic

Para crear una variable de automatización y una instancia de un objeto para esa variable, se pueden utilizar dos métodos: **Dim** o **CreateObject**.

### <a name="dim"></a>Dim

Se puede utilizar la palabra clave **New** con **Dim** para declarar y crear instancias de los objetos ADO en un solo paso:

```vb 
 
Dim conn As New ADODB.Connection 
```

Asimismo, la declaración de la instrucción **Dim** y la creación de instancias de objetos pueden constar de dos pasos:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> No es necesario utilizar explícitamente el identificador de programa ADODB con la instrucción **Dim**, suponiendo que se ha hecho correctamente referencia a la biblioteca de ADO en el proyecto. Sin embargo, su uso garantiza que no habrá conflictos de nomenclatura con otras bibliotecas.
> 
> Por ejemplo, si se incluyen referencias a ADO y DAO en el mismo proyecto, se deberá incluir un calificador para especificar el modelo de objetos que se va a usar cuando se creen instancias de los objetos **Recordset**, como en el siguiente código:  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

Con el método **CreateObject**, la declaración y la creación de instancias de objetos deben constar de dos pasos diferenciados:

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Los objetos cuyas instancias se crean con **CreateObject** se enlazan en tiempo de ejecución, lo que significa que no tienen establecimiento inflexible de tipos y que la opción para completar la línea de comandos no está habilitada. Sin embargo, permite omitir la referencia a la biblioteca de ADO desde el proyecto y permite crear instancias de versiones específicas de los objetos. Por ejemplo:

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Para ello, también se puede crear específicamente una referencia a la versión 2.0 de la Biblioteca de tipos de ADO y crear el objeto.

La creación de instancias de los objetos con el método **CreateObject** suele ser más lenta que cuando se utiliza la instrucción **Dim**.

## <a name="handling-events"></a>Administración de eventos

Para controlar eventos de ADO en Microsoft Visual Basic, debe declarar una variable de nivel de módulo mediante la palabra clave **WithEvents.** La variable se puede declarar sólo como parte de un módulo de clase y se debe declarar en el nivel de módulo. Para obtener una explicación más completa del control de eventos de ADO, vea [el Capítulo 7: Controlar eventos de ADO](chapter-7-handling-ado-events.md).

## <a name="visual-basic-examples"></a>Visual Basic ejemplos

La documentación de ADO incluye numerosos ejemplos de Visual Basic. Para obtener más información, vea [ejemplos de código de ADO en Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).


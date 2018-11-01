---
title: Utilizar ADO con Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8644bd4f5b1a19848689adf92dca91ba30f324c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889850"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Uso de ADO con Microsoft Visual Basic


**Se aplica a**: Access 2013, Office 2013

Configurar un proyecto de ADO y escribir código de ADO es un procedimiento similar en Visual Basic y Visual Basic para Aplicaciones. En este tema se aborda el uso de ADO con Visual Basic y Visual Basic para Aplicaciones, así como las diferencias.

## <a name="referencing-the-ado-library"></a>Hacer referencia a la biblioteca de ADO

El proyecto debe hacer referencia a la biblioteca de ADO.

**Para hacer referencia a ADO desde Microsoft Visual Basic**

1.  En Visual Basic, en el menú **Proyecto**, seleccione **Referencias**.

2.  Seleccione **Biblioteca de Microsoft ActiveX Data Objects x.x** en la lista. Compruebe que estén seleccionadas al menos las siguientes bibliotecas:
    
    - Visual Basic para Aplicaciones
    
    - Objetos y procedimientos del motor en tiempo de ejecución de Visual Basic
    
    - Objetos y procedimientos de Visual Basic
    
    - Automatización OLE

3.  Haga clic en **Aceptar**.

ADO se puede utilizar con la misma facilidad con Visual Basic para Aplicaciones mediante, por ejemplo, Microsoft Access.

**Para hacer referencia a ADO desde Microsoft Access**

1.  En Microsoft Access, seleccione o cree un módulo en la pestaña **Módulos** de la ventana **Base de datos**.

2.  En el menú **Herramientas**, seleccione **Referencias**.

3.  Seleccione **Biblioteca de Microsoft ActiveX Data Objects x.x** en la lista. Compruebe que estén seleccionadas al menos las siguientes bibliotecas:
    
    - Visual Basic para Aplicaciones
    
    - Biblioteca de objetos de Microsoft Access 11.0 (o posterior)

4.  Haga clic en **Aceptar**.

## <a name="creating-ado-objects-in-visual-basic"></a>Crear objetos ADO en Visual Basic

Para crear una variable de automatización y una instancia de un objeto para esa variable, se pueden utilizar dos métodos: **Dim** o **CreateObject**.

## <a name="dim"></a>Dim

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
> <P>No es necesario utilizar explícitamente el identificador de programa ADODB con la instrucción <STRONG>Dim</STRONG>, suponiendo que se ha hecho correctamente referencia a la biblioteca de ADO en el proyecto. Sin embargo, su uso garantiza que no habrá conflictos de nomenclatura con otras bibliotecas.</P>



Por ejemplo, si se incluyen referencias a ADO y DAO en el mismo proyecto, se deberá incluir un calificador para especificar el modelo de objetos que se va a usar cuando se creen instancias de los objetos **Recordset**, como en el siguiente código:  
Dim adoRS As ADODB. Conjunto de registros  
  
Dim daoRS As DAO. Conjunto de registros

## <a name="createobject"></a>CreateObject

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

## <a name="handling-events"></a>Controlar eventos

Para controlar los eventos de ADO en Microsoft Visual Basic, es preciso declarar una variable en el nivel de módulo mediante la palabra clave **WithEvents**. La variable se puede declarar únicamente como parte de un módulo de clase y debe declararse en el nivel de módulo. Para obtener una descripción más completa de cómo controlar los eventos de ADO, vea [Capítulo 7: Controlar eventos de ADO](chapter-7-handling-ado-events.md).

## <a name="visual-basic-examples"></a>Ejemplos de Visual Basic

La documentación de ADO incluye numerosos ejemplos de Visual Basic. Para obtener más información, vea [ejemplos de código de ADO en Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).


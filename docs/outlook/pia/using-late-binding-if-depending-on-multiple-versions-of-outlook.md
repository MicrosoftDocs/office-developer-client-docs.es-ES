---
title: Uso del enlace en tiempo de ejecución cuando se depende de varias versiones de Outlook
TOCTitle: Using late binding if depending on multiple versions of Outlook
ms:assetid: 4e5412a0-d0f8-4819-ba0f-f36ba885f8f6
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610234(v=office.15)
ms:contentKeyID: 55119791
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 866faab04e8fcac1d91b233f801f05c023ac2164
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407075"
---
# <a name="using-late-binding-if-depending-on-multiple-versions-of-outlook"></a>Uso del enlace en tiempo de ejecución cuando se depende de varias versiones de Outlook

Los complementos administrados de Outlook que usan el ensamblado de interoperabilidad primario (PIA) de Outlook se compilan con la información de tipo que proporciona el PIA. Este **enlace anticipado** de información de tipo para métodos y propiedades permite al compilador realizar comprobaciones de tipo y sintaxis para garantizar que se pasan los parámetros correctos de número y tipo al método o propiedad, y que el valor devuelto es del tipo esperado. 

Sin embargo, el enlace anticipado tiene la desventaja de que presenta una incompatibilidad de versión si el complemento llama a un método o propiedad que tenga una declaración diferente en una versión anterior. Por ejemplo, agregar nuevos métodos y propiedades o modificar miembros existentes de un objeto puede alterar el diseño binario del objeto y causar problemas con un complemento administrado que usa la información de tipo más reciente para automatizar una versión anterior de Outlook. 

En esos casos, el **enlace en tiempo de ejecución** espera hasta el tiempo de ejecución para enlazar las llamadas a propiedades y métodos de los objetos. El enlace en tiempo de ejecución puede evitar complicaciones de tipos que son diferentes en las diferentes versiones de Outlook, y resulta especialmente útil al escribir los complementos que dependen de varias versiones de Outlook.

El enlace en tiempo de ejecución implica una llamada del complemento a la interfaz [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch) implementada por Outlook. Para usar el enlace en tiempo de ejecución en Visual C\#, use el método [System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2). Este método llama a los métodos [IDispatch::GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) y [IDispatch::Invoke](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para enlazar con las propiedades y los métodos de Outlook. El método IDispatch::GetIDsOfNames permite a Visual C\# preguntar a un objeto qué métodos y propiedades admite, y el método IDispatch::Invoke permite a Visual C\# llamar a esos métodos y propiedades. 

<!-- PAGES 404 
For more information about using late binding in C\#, see [KB 302902: Binding for Office Automation Servers with Visual C\# .NET](https://go.microsoft.com/fwlink/?linkid=88971). For more information about using late binding in Visual Basic, see [KB 304661: How to Use Visual Basic .NET for Binding for Office Automation Servers](https://go.microsoft.com/fwlink/?linkid=88972).

Note that late binding requires obtaining a DispID for every method or property, so late binding generally does not perform as well as early binding. For more information about how early binding compares with late binding, see [KB 245115: Using Early Binding and Late Binding in Automation](https://go.microsoft.com/fwlink/?linkid=88973). -->

## <a name="see-also"></a>Vea también

- [Introducción a la interoperabilidad entre COM y .NET](introduction-to-interoperability-between-com-and-net.md)


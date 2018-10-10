---
title: Objetos de Outlook PIA
TOCTitle: Objects in the Outlook PIA
ms:assetid: 1be732a6-d6da-4fa0-beaa-accf35db12d6
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609459(v=office.15)
ms:contentKeyID: 55119778
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 434be5dc9193beaf9723530c6d963ed0a96d8884
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407033"
---
# <a name="objects-in-the-outlook-pia"></a>Objetos de Outlook PIA

Al explorar el ensamblado de interoperabilidad primario de Outlook (PIA) en un explorador de objetos, es posible que observe que muchas interfaces y clases tienen nombres que hacen referencia a objetos familiares en el modelo de objetos de Outlook. Algunos objetos del modelo de objetos tienen una correspondencia de uno a uno con las interfaces en el PIA. 

Por ejemplo, el objeto **AddressEntry** está asignado a la interfaz [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) y el objeto **AddressList** está asignado a la interfaz [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) en el PIA. 

Sin embargo, la mayoría de los demás objetos tienen una asignación de uno a varios en el PIA. Esta asignación de uno a varios se aplica a algunos de los objetos que existían antes de Microsoft Office Outlook 2007 y a todos los objetos añadidos después de Outlook 2007. En este tema se describen los delegados, clases e interfaces .NET típicos que se asignan a un objeto COM y describe cómo obtener acceso a un objeto en el PIA de Outlook. También se describen algunas excepciones en el PIA de Outlook en las que los objetos están ocultos o en desuso en el modelo de objetos basado en COM de Outlook.

## <a name="helper-objects"></a>Objetos auxiliares

Esta sección muestra las clases de asistentes típicos de un objeto en el Outlook PIA usando el objeto **FormRegion** como ejemplo. El objeto **FormRegion** se agregó al modelo de objetos en Outlook 2007. En relación con el objeto **FormRegion** del PIA están las interfaces, clases y delegados, como se muestra en la ilustración 1.

**Figura 1. El objeto FormRegion representado en el modelo de objetos de Outlook y en el PIA de Outlook**

![El objeto FormRegion representado en el modelo de objetos de Outlook y en el PIA de Outlook](media/pia-outlook-object-model.gif)

La interfaz que se usa más menudo para obtener acceso al objeto **FormRegion** y sus miembros de eventos, propiedades y métodos es la interfaz [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)). Sin embargo, no debe considerar la interfaz .NET **FormRegion** como una imagen reflejada exacta del objeto COM **FormRegion**; si mira el Examinador de objetos en Visual Studio, verá que la interfaz **FormRegion** hereda de otra interfaz, la interfaz [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)). De hecho, la interfaz **FormRegion** es tan solo una de las pocas interfaces y clases que se producen al crear el PIA de Outlook basado en la biblioteca de tipos COM.

Para crear un PIA de Outlook, Outlook usa el Importador de la biblioteca de tipos (TLBIMP) en .NET Framework para convertir las definiciones de tipos en la biblioteca de tipos COM en definiciones equivalentes en el ensamblado de Common Language Runtime. En COM, el objeto **FormRegion** es una coclase que consta de las siguientes dos interfaces que definen las interfaces que el objeto **FormRegion** implementa:

- La interfaz principal **\_FormRegion**

- La interfaz de eventos [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))

TLBIMP importa directamente **\_FormRegion** y **FormRegionEvents** desde la biblioteca de tipos.

En lugar de importar la interfaz primaria y la interfaz de eventos, TLBIMP crea una interfaz de .NET que tiene el mismo nombre que el objeto COM, y una clase .NET que usa el nombre del objeto y le agrega "Class". En el caso del objeto **FormRegion**, TLBIMP crea lo siguiente:

- La interfaz .NET **FormRegion**

- La clase .NET [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))

En las interfaces de .NET y las clases .NET mencionadas en este tema, siempre se usa la interfaz de .NET que crea TLBIMP para tener acceso a un objeto. Por ejemplo, para obtener acceso a un objeto **FormRegion** en VB, siempre se usa la interfaz de **FormRegion**, como en el siguiente ejemplo de código:

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
Sub DemoFormRegion(ByVal Region As Outlook.FormRegion)
    Dim MyFormRegion As Outlook.FormRegion = Region
    ' Additional method code here
End Sub
```

<br/>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook; 
void DemoFormRegion(Outlook.FormRegion region) 
{
    Outlook.FormRegion myFormRegion = region; 
    // Additional method code here
}
```

Para obtener información acerca de la finalidad de la interfaz principal y la clase .NET que TLBIMP importa y crea respectivamente, consulte [Métodos y propiedades del PIA de Outlook](methods-and-properties-in-the-outlook-pia.md). Para obtener información acerca de la finalidad de las interfaces relacionadas con eventos, clases de auxiliares de receptor, consulte [Eventos de Outlook PIA](events-in-the-outlook-pia.md).

## <a name="deprecated-objects"></a>Objetos en desuso

Los objetos en desuso en la biblioteca de tipos se muestran en el PIA de Outlook. Por ejemplo, los objetos **\_DDocSiteControl** y **\_DRecipientControl** están ocultos en la biblioteca de tipos, pero se muestran en el PIA.

Otro ejemplo de un objeto en desuso es el objeto **MAPIFolder**. A partir de Outlook 2007, el objeto **Folder** reemplaza el objeto **MAPIFolder** en el modelo de objetos. Las soluciones existentes deben reemplazar las referencias a **MAPIFolder** de **Folder**, y todas las soluciones nuevas para Outlook 2007 y posteriores deberían usar solo el objeto **Folder**. En el caso de soluciones no administradas, el Examinador de objetos del Editor de Visual Basic ya no muestra el objeto **MAPIFolder**, ni siquiera como objeto oculto. 

Para soluciones administradas, aunque el PIA de Outlook muestra una interfaz [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) a través de la que accede al objeto **Folder** y sus miembros, el PIA de Outlook también expone [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) como una interfaz que define los miembros del objeto **Folder**.

## <a name="see-also"></a>Vea también

- [Relación del PIA de Outlook con el modelo de objetos](relating-the-outlook-pia-with-the-object-model.md)



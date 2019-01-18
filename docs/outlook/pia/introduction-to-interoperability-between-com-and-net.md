---
title: Introducción a la interoperabilidad entre COM y .NET
TOCTitle: Introduction to interoperability between COM and .NET
ms:assetid: 6b2d099a-ec6f-4099-aaf6-e61003fe5a32
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610378(v=office.15)
ms:contentKeyID: 55119776
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b19135900974c3fa379aa9f4acb18ee98a2f8c5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709190"
---
# <a name="introduction-to-interoperability-between-com-and-net"></a>Introducción a la interoperabilidad entre COM y .NET

El desarrollo de .NET y del modelo de objetos componentes (COM) tienen sistemas y mecanismos muy diferentes para la administración de la duración de objeto, la creación de la interfaz y la herencia de la interfaz. 

Por ejemplo, un tipo **Variant** en COM es un tipo de datos **System.Object** en .NET Framework. Para crear un objeto, un cliente COM llama a [CoCreateInstance](https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), mientras que un cliente administrado puede usar palabras clave como nuevo o Nuevo que están integradas en un lenguaje de programación administrado. 

Mientras que COM no admite la herencia clásica y un cliente COM administra un número de referencia interna proporcionado por [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) para liberar una coclase, un cliente administrado depende del recolector de elementos no utilizados de Common Language Runtime (CLR) proporcionado por .NET Framework para liberar un objeto. 

Teniendo en cuenta estas diferencias entre el desarrollo de COM y .NET, desarrollar un cliente administrado en un modelo de objetos COM requiere un mecanismo que solucione estas diferencias. El contenedor invocable en tiempo de ejecución (RCW) es un mecanismo que fomenta la comunicación transparente entre COM y el modelo de programación administrado.

Este tema proporciona una descripción avanzada de cómo el RCW facilita la comunicación entre COM y el modelo de programación administrado. Tenga en cuenta que aunque este tema usa Visual Studio para ilustrar el mecanismo RCW, puede usar un ensamblado de interoperabilidad fuera de Visual Studio para desarrollar un cliente administrado.

## <a name="facilitating-interoperability-the-interop-assembly-and-rcw"></a>Facilitar la interoperabilidad: el ensamblado de interoperabilidad y RCW

### <a name="compile-time"></a>Tiempo de compilación

Un ensamblado de interoperabilidad define interfaces administradas que se asignan a una biblioteca de tipos basada en COM y con las que un cliente administrado puede interactuar. Para usar un ensamblado de interoperabilidad en Visual Studio, primero agregue una referencia al componente COM correspondiente. Visual Studio genera automáticamente una copia local del ensamblado de interoperabilidad. El ensamblado de interoperabilidad contiene un espacio de nombres, en el que hay una interfaz administrada equivalente de cada objeto COM en el modelo de objetos COM. 

La figura 1 muestra un cliente administrado que desea usar una biblioteca de tipos COM que define la coclase X. El cliente administrado llama a la clase X, que es la interfaz administrada equivalente para coclase X, según se define en el ensamblado de interoperabilidad. En el momento de compilación, se compila el proyecto administrado con información acerca de la clase X del ensamblado de interoperabilidad.

**Figura 1. Una aplicación administrada con un ensamblado de interoperabilidad que interopera una biblioteca de tipos no administrada**

![Una aplicación administrada con un ensamblado de interoperabilidad que interopera una biblioteca de tipos no administrada](media/pia-unmanaged-type-library.gif)
  
En general, siempre que establezca una referencia a una biblioteca de tipos, Visual Studio generará una copia de un ensamblado de interoperabilidad para esa biblioteca de tipos. Puede existir cualquier cantidad de ensamblados de interoperabilidad para describir el mismo tipo de COM. Sin embargo, una biblioteca de tipos puede tener solo un ensamblado de interoperabilidad primario (PIA), que es el ensamblado de interoperabilidad publicado por la biblioteca de tipos. A diferencia de otros ensamblados de interoperabilidad, el PIA no se genera cada vez que agrega una referencia en Visual Studio. En lugar de ello, debe instalar el PIA en la memoria caché global de ensamblados (GAC) una sola vez en un equipo. Cuando agrega una referencia a la biblioteca de tipos, Visual Studio carga el PIA automáticamente.

Para programar una solución administrada de Outlook, debe usar Outlook PIA. Para incorporar información de Outlook PIA en un complemento administrado, primero debe instalar Outlook PIA en la GAC. Si usa Visual Studio para crear un proyecto administrado, después de agregar una referencia a la biblioteca de tipos de Outlook, Visual Studio carga el PIA. En el examinador de objetos, en el espacio de nombres Microsoft.Office.Interop.Outlook, puede ver las interfaces administradas que tienen nombres correspondientes a los objetos en el modelo de objetos de Outlook. Por ejemplo, la interfaz Account se corresponde con el objeto **Account** en el modelo de objetos de Outlook. Al compilar el proyecto administrado, esta información se incluye en el ejecutable.

### <a name="run-time"></a>Tiempo de ejecución

En el momento de la ejecución, con la información proporcionada por un ensamblado de interoperabilidad, CLR de .NET Framework crea un RCW para cada coclase con la que interactúa el cliente administrado. Tenga en cuenta que el tiempo de ejecución crea solo un RCW para cada coclase, independientemente de cuántas interfaces haya obtenido el cliente de la coclase. El RCW es un tipo de clase de .NET Framework que se ajusta alrededor de la coclase de COM. El RCW realiza un seguimiento de las instancias de la coclase y libera referencias a ellas solo cuando el cliente ya no necesita el RCW. De este modo, un cliente administrado no tiene que administrar la duración de un objeto como lo haría un cliente no administrado en COM.

La figura 2 ilustra un RCW que intercepta una llamada de la API de un cliente administrado en tiempo de ejecución y, mediante el uso de información del ensamblado de interoperabilidad, asigna de forma transparente la llamada a la API correspondiente en la coclase de COM. En el siguiente proceso se describe cómo se produce:

1.  El cliente administrado llama al método A' de la clase X' como se define en el ensamblado de interoperabilidad de una biblioteca de tipos COM.

2.  Si todavía no existe un RCW para la clase X', el tiempo de ejecución de Framework usa información del ensamblado de interoperabilidad y crea un RCW para la clase X'.

3.  El RCW intercepta la llamada al método A', traduce los argumentos a los tipos COM correspondientes e invoca el método A de la coclase X como se define en la biblioteca de tipos COM.

**Figura 2. Un RCW intercepta una llamada de un ejecutable administrado y la asigna a una coclase de una biblioteca de tipos no administrados**

![Un RCW intercepta una llamada de un ejecutable administrado y la asigna a una coclase de una biblioteca de tipos no administrados](media/pia-unmanaged-type-library-2.gif)
  

## <a name="see-also"></a>Vea también

- [Por qué usar Outlook PIA](why-use-the-outlook-pia.md)
- [Instalación del PIA de Outlook y referencia a él](installing-and-referencing-the-outlook-pia.md)


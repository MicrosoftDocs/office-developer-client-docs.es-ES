---
title: Por qué usar el PIA de Outlook
TOCTitle: Why use the Outlook PIA
ms:assetid: 5cc9085e-7c97-4698-8cb9-e33e427c02e7
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb645534(v=office.15)
ms:contentKeyID: 55119773
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7e36a0de33ea3e23d53ff82b31cc937dff0d7e14
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406060"
---
# <a name="why-use-the-outlook-pia"></a>Por qué usar el PIA de Outlook

Desde Outlook 98, Outlook ofrece un modelo de objetos para que los desarrolladores integran la funcionalidad de Outlook en una aplicación, amplíen Outlook o automaticen Outlook. Este modelo de objetos está diseñado para funcionar con la tecnología de Modelo de objetos componentes (COM). Por lo general, los desarrolladores de la aplicación de Outlook desarrollaban soluciones COM usando Visual Basic para Aplicaciones (VBA) y Visual Basic. Sin embargo, las soluciones de Outlook desarrolladas con VBA tienen limitaciones en cuanto a la implementación, especialmente en entornos empresariales, y es difícil actualizarlas cuando se implementan.

.NET Framework ofrece un amplio conjunto de bibliotecas de clases y tecnologías compatibles que resuelven muchas de las limitaciones de los complementos COM y VBA. Sin embargo, una aplicación administrada necesita un puente entre los entornos .NET y COM para programar en un modelo de objeto COM. Un ensamblado de interoperabilidad es un contenedor COM que actúa como puente. Por lo tanto, ahora se desarrollan más soluciones Outlook como aplicaciones administradas que se basan en un ensamblado de interoperabilidad. Para obtener más información sobre cómo los ensamblados de interoperabilidad facilitan la interoperabilidad entre .NET y COM, vea [Introducción a la interoperabilidad entre COM y .NET](introduction-to-interoperability-between-com-and-net.md).

Un ensamblado de interoperabilidad describe tipos COM y permite que el código administrado interactúe con un modelo de objetos COM. Puede existir cualquier cantidad de ensamblados de interoperabilidad para describir un determinado tipo COM. Como editor de la biblioteca de tipos, Outlook proporciona un ensamblado de interoperabilidad primario (PIA) que contiene la descripción oficial del modelo de objetos de Outlook basados en COM. En general, se recomienda usar el ensamblado de interoperabilidad primario de Outlook en lugar de depender de un ensamblado de interoperabilidad de otra fuente.

## <a name="using-visual-studio-and-office-developer-tools-for-visual-studio"></a>Usar Visual Studio y Office Developer Tools para Visual Studio

Los desarrolladores pueden crear soluciones de Outlook administradas fuera de Visual Studio, pero usar Visual Studio hace que sea mucho más fácil integrar la funcionalidad de Outlook en código administrado. Gracias a la comodidad y la sencillez de desarrollo, a los desarrolladores de complementos les resulta más fácil migrar de un desarrollo de COM a uno de .NET. En el tiempo de diseño, los desarrolladores pueden usar Office Developer Tools para Visual Studio para crear complementos que tengan acceso al modelo de objetos de Outlook y a .NET Framework. En el tiempo de ejecución, Office Developer Tools para Visual Studio ofrece un cargador para estos complementos: cuando un usuario inicia Outlook, este cargador inicia Common Language Runtime (CLR) y Visual Studio Tools para Office Runtime, y después carga el ensamblado del complemento. El ensamblado puede capturar eventos generados en Outlook.

Visual Studio 2012 instala de manera predeterminada las plantillas de complementos para Office 2010. Para usar Office Developer Tools para Visual Studio para desarrollar complementos administrados para Outlook 2013, debe [descargar](https://aka.ms/officedevtoolsforvs2012) las plantillas para Office 2013.

Para obtener más información sobre Office Developer Tools para Visual Studio, vea [Configurar un equipo para desarrollar soluciones de Office](https://docs.microsoft.com/visualstudio/vsto/how-to-configure-a-computer-to-develop-office-solutions?view=vs-2017). Para obtener más información sobre la programación de complementos administrados para Outlook, vea [Get started programming VSTO Add-ins](https://docs.microsoft.com/visualstudio/vsto/getting-started-programming-vsto-add-ins?view=vs-2017) (Introducción a la programación de complementos VSTO).

## <a name="see-also"></a>Vea también

- [Instalar el PIA de Outlook y hacer referencia a él](installing-and-referencing-the-outlook-pia.md)


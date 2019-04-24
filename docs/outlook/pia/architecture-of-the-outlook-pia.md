---
title: Arquitectura del ensamblado de interoperabilidad primario de Outlook
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 37ecad42b08b96d79d96d62f98e27913a0309971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336529"
---
# <a name="architecture-of-the-outlook-pia"></a>Arquitectura del PIA de Outlook

El ensamblado de interoperabilidad principal (PIA) de Outlook es completamente compatible con el desarrollo con el modelo de objetos de Outlook en el código administrado. No obstante, si visualiza el PIA en un explorador de objetos por primera vez, pueden sorprenderle las múltiples interfaces adicionales que contiene el PIA y el hecho de que no todos los miembros de eventos, propiedades y métodos de un objeto se exponen con la misma interfaz de objeto. Los temas de esta sección describen directrices sobre cómo obtener acceso a los miembros del objeto en el código y dónde debe buscar ayuda para los objetos, métodos, propiedades y eventos.

## <a name="in-this-section"></a>En esta sección

|Tema|Descripción|
|:----|:----------|
|[Relación del PIA de Outlook con el modelo de objetos](relating-the-outlook-pia-with-the-object-model.md) |Describe cómo se asignan los objetos y los miembros del modelo de objetos de Outlook basado en COM a las correspondientes interfaces y clases administradas en el PIA.|
|[Objetos del PIA de Outlook](objects-in-the-outlook-pia.md) |Describe las interfaces, las clases y los delegados .NET típicos que se asignan a un objeto COM y describe cómo obtener acceso a un objeto en el PIA.|
|[Métodos y propiedades del PIA de Outlook](methods-and-properties-in-the-outlook-pia.md) |Describe cómo obtener acceso a los métodos y las propiedades de un objeto de código administrado usando el PIA de Outlook.|
|[Eventos del PIA de Outlook](events-in-the-outlook-pia.md) |Describe las interfaces relacionadas con los eventos, los delegados y las clases auxiliares de receptores en el PIA.|

## <a name="see-also"></a>Vea también

- [Configuración para el uso del PIA de Outlook](setting-up-to-use-the-outlook-pia.md)
- [Desarrollo de complementos de Outlook administrados con el PIA de Outlook](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [How do I... (Outlook 2013 PIA reference)](how-do-i-outlook-2013-pia-reference.md) (¿Cómo se puede... [Referencia a PIA de Outlook 2013])


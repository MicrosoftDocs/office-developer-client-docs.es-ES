---
title: Automatización con Microsoft Access
TOCTitle: Automation with Microsoft Access
description: Microsoft Access es un componente COM que admite la característica Automatización, que anteriormente se denominaba Automatización OLE.
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 9635cdb2a06f610f42e4aa9fc9f998719aebb986
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296965"
---
# <a name="automation-with-microsoft-access"></a>Automatización con Microsoft Access

**Se aplica a:** Access 2013, Office 2013

Microsoft Access es un componente COM compatible con la Automatización, denominada anteriormente Automatización OLE. Microsoft Access admite la Automatización de dos formas. Desde Microsoft Access, puede trabajar con los objetos suministrados por otro componente. Microsoft Access suministra también sus objetos a otros componentes COM.

Puede usar la palabra clave **New** o el método **CreateObject** para crear una nueva instancia de un componente. Puede usar el método **GetObject** para asignar una variable a una instancia existente de un componente.

En Microsoft Access, puede establecer una referencia a la biblioteca de tipos de un componente para mejorar el rendimiento cuando trabaje con ese componente a través de Automatización. Microsoft Access incluye también el Examinador de objetos, una herramienta que le permite ver los objetos de la biblioteca de tipos de otro componente, así como sus métodos y propiedades.

La biblioteca de tipos de Microsoft Access proporciona información sobre los objetos de Microsoft Access a otros componentes. Puede [establecer una referencia](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) a la biblioteca de tipos de Microsoft Access desde un componente y ver sus objetos en el Examinador de objetos.

Para trabajar con los objetos de Microsoft Access a través de Automatización, debe crear una instancia del objeto **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** de Microsoft Access. Por ejemplo, suponga que desea mostrar datos de Microsoft Excel en un formulario o informe de Microsoft Access. Para ejecutar Microsoft Access desde Microsoft Excel, puede usar la palabra clave **New** para crear una instancia del objeto **Application** de Microsoft Access. También puede usar el método **CreateObject** para crear una nueva instancia del objeto **Application** de Microsoft Access, o puede usar el método **GetObject** para apuntar una variable de objeto a una instancia existente de Microsoft Access. Compruebe la documentación del componente para determinar la sintaxis con la que es compatible.

Una vez iniciada una instancia de Microsoft Access, si desea controlar cualquier objeto de Microsoft Access, deberá abrir una base de datos o un proyecto (.adp) en la ventana de Microsoft Access, con el método **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** o **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** para una base de datos, o bien con el método **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** o **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** para un proyecto.

Si sólo ha abierto Microsoft Access como una forma de usar los objetos de acceso a datos proporcionados por Microsoft DAO, no es necesario que abra una base de datos en la ventana de Microsoft Access. Puede usar la propiedad **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** del objeto **Application** de Microsoft Access para tener acceso a los objetos de la biblioteca de objetos del motor de base de datos de Microsoft Office 12.0 Access durante una operación de Automatización.


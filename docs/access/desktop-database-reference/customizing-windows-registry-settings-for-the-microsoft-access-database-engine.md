---
title: Personalización de la configuración del Registro de Windows para el motor de base de datos de Microsoft Access
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 99e2b31cf686895a56e9d70b177314355c1aff3c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945150"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Personalización de la configuración del Registro de Windows para el motor de base de datos de Microsoft Access

**Se aplica a**: Access 2013, Office 2013

Si su aplicación no funciona correctamente con funcionalidad predeterminada del motor de base de datos de Microsoft Access, puede que tenga que cambiar la configuración en el registro de Microsoft Windows que mejor se adapte a sus necesidades. El Registro de Windows también se puede utilizar para ajustar el funcionamiento del controlador ODBD e ISAM instalable.

Puede personalizar la configuración del Registro de Windows de cuatro formas distintas:

- [Use Regedit.exe para sobrescribir la configuración predeterminada](https://msdn.microsoft.com/library/ff193205\(v=office.15\))
- [Creación de una parte en el árbol de registro de la aplicación para administrar la configuración](https://msdn.microsoft.com/library/ff836342\(v=office.15\))
- [Mediante el método SetOption de DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))
- [Usar las propiedades de conexión en el proveedor Microsoft OLE DB para Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))


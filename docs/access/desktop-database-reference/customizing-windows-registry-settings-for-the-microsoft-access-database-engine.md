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
localization_priority: Normal
ms.openlocfilehash: 7cbe8ad56e01249563f7b06c9018d923a96246e9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707363"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Personalización de la configuración del Registro de Windows para el motor de base de datos de Microsoft Access

**Se aplica a**: Access 2013, Office 2013

Si su aplicación no funciona correctamente con funcionalidad predeterminada del motor de base de datos de Microsoft Access, puede que tenga que cambiar la configuración en el registro de Microsoft Windows que mejor se adapte a sus necesidades. El Registro de Windows también se puede utilizar para ajustar el funcionamiento del controlador ODBD e ISAM instalable.

Puede personalizar la configuración del Registro de Windows de cuatro formas distintas:

- [Use Regedit.exe para sobrescribir la configuración predeterminada](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [Creación de una parte en el árbol de registro de la aplicación para administrar la configuración](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [Mediante el método SetOption de DAO](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [Usar las propiedades de conexión en el proveedor Microsoft OLE DB para Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)


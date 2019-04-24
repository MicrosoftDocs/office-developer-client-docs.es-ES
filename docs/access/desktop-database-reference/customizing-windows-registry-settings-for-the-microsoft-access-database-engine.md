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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295124"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="1d09b-102">Personalización de la configuración del Registro de Windows para el motor de base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="1d09b-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="1d09b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d09b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d09b-104">Si la aplicación no funciona correctamente con las funciones predeterminadas del motor de base de datos de Microsoft Access, es posible que tenga que cambiar la configuración del registro de Microsoft Windows para que se ajuste a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="1d09b-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="1d09b-105">El Registro de Windows también se puede utilizar para ajustar el funcionamiento del controlador ODBD e ISAM instalable.</span><span class="sxs-lookup"><span data-stu-id="1d09b-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="1d09b-106">Puede personalizar la configuración del Registro de Windows de cuatro formas distintas:</span><span class="sxs-lookup"><span data-stu-id="1d09b-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- [<span data-ttu-id="1d09b-107">Usar regedit. exe para sobrescribir la configuración predeterminada</span><span class="sxs-lookup"><span data-stu-id="1d09b-107">Using Regedit.exe to overwrite the default settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [<span data-ttu-id="1d09b-108">Crear una parte en el árbol del registro de la aplicación para administrar la configuración</span><span class="sxs-lookup"><span data-stu-id="1d09b-108">Creating a portion in your application's registry tree to manage the settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [<span data-ttu-id="1d09b-109">Usar el método SetOption de DAO</span><span class="sxs-lookup"><span data-stu-id="1d09b-109">Using the SetOption method from DAO</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [<span data-ttu-id="1d09b-110">Uso de las propiedades de conexión en el proveedor de Microsoft OLE DB para Access</span><span class="sxs-lookup"><span data-stu-id="1d09b-110">Using the Connection properties in the Microsoft OLE DB Provider for Access</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)


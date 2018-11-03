---
title: Propiedad DBEngine.IniPath (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fd744f10d212d8ff0f7c78ca72781869ccdcd57e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928764"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="2c052-102">Propiedad DBEngine.IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="2c052-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="2c052-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c052-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c052-104">Establece o devuelve información sobre la clave del Registro de Windows que contiene los valores para el motor de base de datos Microsoft Access (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2c052-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c052-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c052-105">Syntax</span></span>

<span data-ttu-id="2c052-106">*expresión* . IniPath</span><span class="sxs-lookup"><span data-stu-id="2c052-106">*expression* .IniPath</span></span>

<span data-ttu-id="2c052-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="2c052-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c052-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c052-108">Remarks</span></span>

<span data-ttu-id="2c052-p101">Puede configurar el motor de base de datos Microsoft Access con el Registro de Windows. Puede utilizar el Registro para configurar opciones, tales como los archivos DLL de un archivo ISAM instalable.</span><span class="sxs-lookup"><span data-stu-id="2c052-p101">You can configure the Microsoft Access databse engine with the Windows Registry. You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="2c052-p102">Para que esta opción funcione, debe establecer la propiedad **IniPath** antes de que su aplicación llame a cualquier otro código DAO. El ámbito de esta configuración está limitado a la aplicación y no se puede cambiar sin reiniciar ésta.</span><span class="sxs-lookup"><span data-stu-id="2c052-p102">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code. The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="2c052-p103">Utilice también el Registro para proporcionar parámetros de inicialización para algunos controladores de base de datos ISAM instalables. Por ejemplo, para utilizar la versión 4.0 de Paradox, establezca la propiedad **IniPath** como parte del Registro con los parámetros apropiados.</span><span class="sxs-lookup"><span data-stu-id="2c052-p103">You also use the Registry to provide initialization parameters for some installable ISAM database drivers. For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="2c052-115">Esta propiedad reconoce alguno HKEY\_LOCAL\_máquina o HKEY\_LOCAL\_usuario.</span><span class="sxs-lookup"><span data-stu-id="2c052-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="2c052-116">Si no hay ninguna clave de raíz se proporciona, el valor predeterminado es HKEY\_LOCAL\_máquina.</span><span class="sxs-lookup"><span data-stu-id="2c052-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>


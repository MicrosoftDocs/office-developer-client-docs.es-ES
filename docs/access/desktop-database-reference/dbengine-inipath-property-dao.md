---
title: DBEngine.IniPath (DAO)
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
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294298"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="c564b-102">DBEngine.IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="c564b-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="c564b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c564b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c564b-104">Establece o devuelve información sobre la clave del Registro de Windows que contiene los valores para el motor de base de datos Microsoft Access (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c564b-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c564b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c564b-105">Syntax</span></span>

<span data-ttu-id="c564b-106">*expresión* . IniPath</span><span class="sxs-lookup"><span data-stu-id="c564b-106">*expression* .IniPath</span></span>

<span data-ttu-id="c564b-107">*expression* Variable que representa un objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="c564b-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c564b-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c564b-108">Remarks</span></span>

<span data-ttu-id="c564b-109">Puede configurar el motor de base de datos de Microsoft Access con el Windows registro.</span><span class="sxs-lookup"><span data-stu-id="c564b-109">You can configure the Microsoft Access database engine with the Windows Registry.</span></span> <span data-ttu-id="c564b-110">Puede utilizar el Registro para configurar opciones, tales como los archivos DLL de un archivo ISAM instalable.</span><span class="sxs-lookup"><span data-stu-id="c564b-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="c564b-p102">Para que esta opción funcione, debe establecer la propiedad **IniPath** antes de que su aplicación llame a cualquier otro código DAO. El ámbito de esta configuración está limitado a la aplicación y no se puede cambiar sin reiniciar ésta.</span><span class="sxs-lookup"><span data-stu-id="c564b-p102">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code. The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="c564b-p103">Utilice también el Registro para proporcionar parámetros de inicialización para algunos controladores de base de datos ISAM instalables. Por ejemplo, para utilizar la versión 4.0 de Paradox, establezca la propiedad **IniPath** como parte del Registro con los parámetros apropiados.</span><span class="sxs-lookup"><span data-stu-id="c564b-p103">You also use the Registry to provide initialization parameters for some installable ISAM database drivers. For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="c564b-115">Esta propiedad reconoce HKEY \_ LOCAL \_ MACHINE o HKEY LOCAL \_ \_ USER.</span><span class="sxs-lookup"><span data-stu-id="c564b-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="c564b-116">Si no se proporciona ninguna clave raíz, el valor predeterminado es HKEY \_ LOCAL \_ MACHINE.</span><span class="sxs-lookup"><span data-stu-id="c564b-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>


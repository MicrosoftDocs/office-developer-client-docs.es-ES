---
title: Propiedad Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292072"
---
# <a name="handler-property-rds"></a><span data-ttu-id="e6795-102">Propiedad Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="e6795-102">Handler property (RDS)</span></span>

<span data-ttu-id="e6795-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6795-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6795-104">Indica el nombre de un programa de personalización del servidor (controlador) que amplía la funcionalidad de [RDSServer.DataFactory](datafactory-object-rdsserver.md) y de cualquier parámetro utilizado por el *controlador*.</span><span class="sxs-lookup"><span data-stu-id="e6795-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6795-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6795-105">Syntax</span></span>

<span data-ttu-id="e6795-106">*DataControl*. Handler = *String*</span><span class="sxs-lookup"><span data-stu-id="e6795-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="e6795-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6795-107">Parameters</span></span>

|<span data-ttu-id="e6795-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e6795-108">Parameter</span></span>|<span data-ttu-id="e6795-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6795-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e6795-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="e6795-110">*DataControl*</span></span> |<span data-ttu-id="e6795-111">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e6795-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="e6795-112">*String*</span><span class="sxs-lookup"><span data-stu-id="e6795-112">*String*</span></span> |<span data-ttu-id="e6795-113">Valor **string** que contiene el nombre del controlador y los parámetros, todos separados por comas (por ejemplo, "handlerName,parm1,parm2,...,parm *N*" ).</span><span class="sxs-lookup"><span data-stu-id="e6795-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="e6795-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6795-114">Remarks</span></span>

<span data-ttu-id="e6795-115">Esta propiedad admite personalización, una funcionalidad que exige el establecimiento de la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="e6795-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="e6795-p101">El nombre del controlador y sus parámetros, si los hubiera, se separan mediante comas (","). La aparición de un punto y coma (";") en algún lugar de *String* dará lugar a un comportamiento impredecible. Puede escribir su propio controlador siempre que admita la interfaz **IDataFactoryHandler**.</span><span class="sxs-lookup"><span data-stu-id="e6795-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="e6795-p102">El nombre del controlador predeterminado es **MSDFMAP.Handler**, mientras que su parámetro predeterminado es un archivo de personalización denominado **MSDFMAP.INI**. Utilice esta propiedad para llamar a archivos de personalización alternativos creados por el administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e6795-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="e6795-121">La alternativa a establecer la **propiedad Handler** es especificar un controlador y parámetros en la [propiedad ConnectionString;](connectionstring-property-ado.md) es decir, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="e6795-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

